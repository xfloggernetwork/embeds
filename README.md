# XFlogger Network Embeds

###Querying Tags from the xFloggerNetwork
All content on the xFloggerNetwork is tagged. You can query those tags using http://www.xfloggernetwork.com/action/json-export/tags. Tags will be returned as an array of json objects in the form of:

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
