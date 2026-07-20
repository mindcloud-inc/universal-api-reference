# WaiverFile: List Sample New Waivers

Retrieves sample new waivers from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-waivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-waivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-waivers?${params}`, {
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
      "_attachments": [
        {}
      ],
      "_images": [
        {}
      ],
      "_participants": [
        {}
      ],
      "_waiverEvent": {},
      "_waiverForm": {},
      "_WPObjectStatus": 1,
      "me": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_attachments` | array<object> |  |
| `_images` | array<object> |  |
| `_participants` | array<object> |  |
| `_waiverEvent` | object |  |
| `_waiverForm` | object |  |
| `_WPObjectStatus` | number |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /sampledata/newwaiver` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sample-new-waivers.md) for the provider-specific parameters and requirements.

