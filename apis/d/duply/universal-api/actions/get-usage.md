# Duply: Get Usage

Retrieves your current usage from Duply.

```
GET https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cycleImageAPIRequest": 1,
      "cycleImageFormRequest": 1,
      "cycleImageTotalSize": {
        "jpg": 1,
        "other": 1,
        "png": 1,
        "thumb": 1
      },
      "cycleVideoRequest": 1,
      "cycleVideoTotalLength": {
        "mp4": 1,
        "webm": 1
      },
      "formShare": 1,
      "space": {
        "assets": {},
        "file": {}
      },
      "subscriptionInfo": {
        "end": {},
        "endTrial": {},
        "isTrial": true,
        "type": "string"
      },
      "subscriptionLimit": {
        "isAllowAPI": true,
        "isAllowAPIThumb": true,
        "isAllowAPITransparent": true,
        "isAllowBrandKit": true,
        "isAllowBrandKitColors": true,
        "isAllowBrandKitFonts": true,
        "isAllowBrandKitLogos": true,
        "isAllowDownloadCustomSize": true,
        "isAllowDownloadTransparent": true,
        "isAllowFolder": true,
        "isAllowFormShare": true,
        "isAllowGenerateVideo": true,
        "isAllowTeam": true,
        "isAllowURL": true,
        "maxBandwidthTotal": 1,
        "maxBrandKitFonts": 1,
        "maxFormDownloadRequest": 1,
        "maxFormShare": 1,
        "maxImageAPIRequest": 1,
        "maxImageRequest": 1,
        "maxTemplates": 1,
        "maxVideoLength": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cycleImageAPIRequest` | number |  |
| `cycleImageFormRequest` | number |  |
| `cycleImageTotalSize.jpg` | number |  |
| `cycleImageTotalSize.other` | number |  |
| `cycleImageTotalSize.png` | number |  |
| `cycleImageTotalSize.thumb` | number |  |
| `cycleVideoRequest` | number |  |
| `cycleVideoTotalLength.mp4` | number |  |
| `cycleVideoTotalLength.webm` | number |  |
| `formShare` | number |  |
| `space.assets` | object |  |
| `space.file` | object |  |
| `subscriptionInfo.end` | object |  |
| `subscriptionInfo.endTrial` | object |  |
| `subscriptionInfo.isTrial` | boolean |  |
| `subscriptionInfo.type` | string |  |
| `subscriptionLimit.isAllowAPI` | boolean |  |
| `subscriptionLimit.isAllowAPIThumb` | boolean |  |
| `subscriptionLimit.isAllowAPITransparent` | boolean |  |
| `subscriptionLimit.isAllowBrandKit` | boolean |  |
| `subscriptionLimit.isAllowBrandKitColors` | boolean |  |
| `subscriptionLimit.isAllowBrandKitFonts` | boolean |  |
| `subscriptionLimit.isAllowBrandKitLogos` | boolean |  |
| `subscriptionLimit.isAllowDownloadCustomSize` | boolean |  |
| `subscriptionLimit.isAllowDownloadTransparent` | boolean |  |
| `subscriptionLimit.isAllowFolder` | boolean |  |
| `subscriptionLimit.isAllowFormShare` | boolean |  |
| `subscriptionLimit.isAllowGenerateVideo` | boolean |  |
| `subscriptionLimit.isAllowTeam` | boolean |  |
| `subscriptionLimit.isAllowURL` | boolean |  |
| `subscriptionLimit.maxBandwidthTotal` | number |  |
| `subscriptionLimit.maxBrandKitFonts` | number |  |
| `subscriptionLimit.maxFormDownloadRequest` | number |  |
| `subscriptionLimit.maxFormShare` | number |  |
| `subscriptionLimit.maxImageAPIRequest` | number |  |
| `subscriptionLimit.maxImageRequest` | number |  |
| `subscriptionLimit.maxTemplates` | number |  |
| `subscriptionLimit.maxVideoLength` | number |  |

## Native endpoint

Through the native Duply API, this operation is `GET /usage` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

