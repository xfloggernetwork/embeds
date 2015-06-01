# XFlogger Network Embeds


###Querying latest videos
You can query the latest videos from the xFloggerNetwork by using http://www.xfloggernetwork.com/action/json-export/videos/. This endpoint will return a JSON object in the form of:

    {
        total: 100000,
        count: 2,
        pages: 50000,
        videos: [
            {
                ID: 2,
                title: "Video Title 2",
                description: "Description",
                date: "2015-06-01 22:46:23",
                thumbnail: "http://www.xfloggernetwork.com/xxx/thumbnail.jpg",
                sprite: "http://www.xfloggernetwork.com/xxx/sprite.jpg",
                tags: [ "Tag1", "Tag2" ],
                tagIds: [ 1, 2 ],
                length: 125,
                lengthFormatted: "2:05",
                embed: "<iframe src='http://www.xfloggernetwork.com/video/xxx/video2.html'></iframe>"
            },
            {
                ID: 1,
                title: "Video Title 1",
                description: "Description",
                date: "2015-06-01 22:46:23",
                thumbnail: "http://www.xfloggernetwork.com/xxx/thumbnail.jpg",
                sprite: "http://www.xfloggernetwork.com/xxx/sprite.jpg",
                tags: [ "Tag1", "Tag2" ],
                tagIds: [ 1, 2 ],
                length: 135,
                lengthFormatted: "2:15",
                embed: "<iframe src='http://www.xfloggernetwork.com/video/xxx/video1.html'></iframe>"
            }
        ]
    }

Urls can take the form of `http://www.xfloggernetwork.com/action/json-export/videos/{PAGE}/{COUNT_PER_PAGE}/` where `PAGE` defaults to 1 and `COUNT_PER_PAGE` defaults to 20 if they aren't provided. Here is an example of page 2 containing 10 videos per page http://www.xfloggernetwork.com/action/json-export/videos/2/10/.

###Querying Tags from the xFloggerNetwork
All content on the xFloggerNetwork is tagged. You can query those tags using http://www.xfloggernetwork.com/action/json-export/tags/. Tags will be returned as an array of JSON objects in the form of:

    [
        {
            ID: 1,
            count: 1000,
            name: "Tag1"
        },
        {
            ID: 2,
            count: 1234,
            name: "Tag2"
        }
    ]
where `ID` will hold the tag_id, `count` will hold the number of videos tagged, and `name` as the name for the tag.

###Querying Tagged videos from the xFloggerNetwork
You can get the latest videos for a tag using `http://www.xfloggernetwork.com/action/json-export/tagged-videos/{TAG_ID}/{PAGE}/{COUNT_PER_PAGE}/` where `TAG_ID` is a valid ID returned by a call to http://www.xfloggernetwork.com/action/json-export/tags/, `PAGE` defaults to 1 and `COUNT_PER_PAGE` defaults to 20 if they aren't provided. Here is an example of page 2 containing 10 videos per page from Tag1 http://www.xfloggernetwork.com/action/json-export/videos/1/2/10/. This url returns data in the same format as if you were querying the latest videos as shown above.
