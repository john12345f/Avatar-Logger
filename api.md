# API

### Avatars

The avatars API will always return a json array which can be deserialized to the following class
```
    public class Avatar
    {
        public string id { get; set; }
        public string name { get; set; }
        public string description { get; set; }
        public string authorId { get; set; }
        public string authorName { get; set; }
        public string assetUrl { get; set; }
        public List<string> tags { get; set; }
        public string imageUrl { get; set; }
        public string thumbnailImageUrl { get; set; }
        public string releaseStatus { get; set; }
        public List<UnityPackage> unityPackages { get; set; }
        public int version { get; set; }
    }
    
    public class UnityPackage
    {
        public string id { get; set; }
        public string unityVersion { get; set; }
        public string unitySortNumber { get; set; }
        public int assetVersion { get; set; }
        public string platform { get; set; }
        public DateTime created_at { get; set; }
        public object assetUrl { get; set; }
    }
```

The avatars API has the following endpoints:
##### `/avatars/search/author/id/{id}`
Returns all avatars by the author. 
Will return a empty array if no avatars are found (`[]`).
##### `/avatars/search/name/{search term}`
Returns 300 avatars the include the given search term.
Will return a empty array if no avatars are found (`[]`).
#### `/avatars/id/{id}`
Returns a single Avatar object.
Will return nothing when the avatar is not found.


### Users

The users API will always return a json array which can be deserialized to the following class
```
    public class User
    {
        public string id { get; set; }
        public string username { get; set; }
        public string displayName { get; set; }
        public string userIcon { get; set; }
        public string bio { get; set; }
        public List<string> bioLinks { get; set; }
        public string profilePicOverride { get; set; }
        public string statusDescription { get; set; }
        public string currentAvatarImageUrl { get; set; }
        public string currentAvatarThumbnailImageUrl { get; set; }
        public string fallbackAvatar { get; set; }
        public string state { get; set; }
        public List<string> tags { get; set; }
        public string developerType { get; set; }
        public string last_login { get; set; }
        public string last_platform { get; set; }
        public bool allowAvatarCopying { get; set; }
        public string status { get; set; }
        public string date_joined { get; set; }
    }
```

##### `/users/id/{id}`
Returns a single User object.
Will return nothing when the user is not found.
##### `/users/search/name/{search term}`
Returns 300 users the include the given search term.
Will return a empty array if no users are found (`[]`).


### Worlds

The worlds API will always return a json array which can be deserialized to the following class
```
    public class World
    {
        public string id { get; set; }
        public string name { get; set; }
        public string description { get; set; }
        public bool featured { get; set; }
        public string authorId { get; set; }
        public string authorName { get; set; }
        public int capacity { get; set; }
        public List<string> tags { get; set; }
        public string releaseStatus { get; set; }
        public string imageUrl { get; set; }
        public string thumbnailImageUrl { get; set; }
        public string assetUrl { get; set; }
        public int version { get; set; }
    }
```

##### `/worlds/id/{id}`
Returns a single World object.
Will return nothing when the world is not found.
