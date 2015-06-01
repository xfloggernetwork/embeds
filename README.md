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
                embed: "<iframe src='http://www.xfloggernetwork.com/video/xxx/video2.html'></iframe>"
            },
        ]
    }


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

