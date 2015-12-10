#BaconForKotlin

This is a simple kotlin library for interacting with the reddit api.

This library was built out for the very simple usecase of BaconMasher. Thus it is not very full featured.
Still, it provides a cood starting place.

###Usage
```
var service = RedditSessionService(<UserAgentString>, <ThisDeviceUniqueId>, <RedditApplicationId>)
var sub = service.flatMap 
    { 
        it.getRandomSubredditPost("EarthPorn","") 
    }
    .subscribe {
        for(item in it){
            if(item.data is t1){
                //Do something with comment like post
            }else if(item.data is t3){
                //Do something with content post...
            }
        }
    }
```

For more information about using the reddit api please visit: https://www.reddit.com/dev/api

