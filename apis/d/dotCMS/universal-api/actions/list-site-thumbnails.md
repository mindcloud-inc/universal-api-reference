# DotCMS: List Site Thumbnails

Retrieves site thumbnail data from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-site-thumbnails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-site-thumbnails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-site-thumbnails?${params}`, {
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
      "entity": [
        {
          "hasThumbnail": true,
          "hostId": "string",
          "hostInode": "string",
          "hostName": "Ava Chen",
          "tagStorage": "string"
        }
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].hasThumbnail` | boolean |  |
| `entity[].hostId` | string |  |
| `entity[].hostInode` | string |  |
| `entity[].hostName` | string |  |
| `entity[].tagStorage` | string |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/site/thumbnails` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-thumbnails.md) for the provider-specific parameters and requirements.

