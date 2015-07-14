# json2notification

[![Download](https://api.bintray.com/packages/8tory/maven/json2notification/images/download.svg) ](https://bintray.com/8tory/maven/json2notification/_latestVersion)
[![JitPack](https://img.shields.io/github/tag/8tory/json2notification.svg?label=JitPack)](https://jitpack.io/#8tory/json2notification)
[![Build Status](https://travis-ci.org/8tory/json2notification.svg)](https://travis-ci.org/8tory/json2notification)
[![Join the chat at https://gitter.im/8tory/json2notification](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/8tory/json2notification?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

![](art/json2notification-2-square-blue-xxhdpi.png)

Convert JSON to Android Notification. This is very useful for push notification (GCM).

## Usage

```java
Notification notification = Json2Notification.from(context).with(json).notification();
NotificationManager notificationManager = (NotificationManager) context.getSystemService(Context.NOTIFICATION_SERVICE);
notificationManager.notify(1, notification);
```

## Installation

via jitpack:

```gradle
repositories {
    maven { url "https://jitpack.io" }
}

dependencies {
    compile 'com.github.8tory:json2notification:-SNAPSHOT'
}
```

via jcenter:

```gradle
repositories {
    jcenter()
}

dependencies {
    compile 'com.infstory:json2notification:1.0.0'
}
```

## Input json format

```json
{
    "android": {
        "notification": {
            "autoCancel": true,
            "bigPictureStyle": {
                "contentTitle": "json2notification",
                "summaryText": "JSON to Android Notification",
                "bigLargeIcon": "http://upload.wikimedia.org/wikipedia/en/b/bc/Wiki.png",
                "bigPicture": "http://upload.wikimedia.org/wikipedia/en/b/bc/Wiki.png"
            },
            "contentInfo": "json2notification.Json2Notification.from(context).with(json).notification();",
            "contentIntent": {
                "getActivity": true,
                "intent": {
                    "action": "android.intent.action.VIEW",
                    "uri": "https://play.google.com/store/apps/details?id=com.story8.android.gallery"
                }
            },
            "contentText": "JSON to Android Notification",
            "contentTitle": "json2notification",
            "deleteIntent": {
                "getActivity": true,
                "intent": {
                    "action": "android.intent.action.VIEW",
                    "uri": "https://play.google.com/store/apps/details?id=com.story8.android.gallery"
                }
            },
            "largeIcon": "http://upload.wikimedia.org/wikipedia/en/b/bc/Wiki.png",
            "smallIcon": "R.drawable.ic_launcher",
            "sound": "content://settings/system/notification_sound"
        }
    }
}
```

## LICENSE

```
Copyright 2015 8tory, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
