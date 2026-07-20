# WaiverFile: Get Site Details

Retrieves site details from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details?${params}`, {
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
      "_doc": {},
      "_labels": [
        {}
      ],
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
| `_doc` | object |  |
| `_labels` | array<object> |  |
| `_WPObjectStatus` | number |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetSiteDetails` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-details.md) for the provider-specific parameters and requirements.

