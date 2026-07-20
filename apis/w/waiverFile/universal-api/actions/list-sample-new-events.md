# WaiverFile: List Sample New Events

Retrieves sample new events from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-sample-new-events?${params}`, {
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
      "_waiverForms": [
        {}
      ],
      "_waivers": [
        {}
      ],
      "_WPObjectStatus": 1,
      "<Category>k__BackingField": {},
      "me": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_waiverForms` | array<object> |  |
| `_waivers` | array<object> |  |
| `_WPObjectStatus` | number |  |
| `<Category>k__BackingField` | object |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /sampledata/newevent` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sample-new-events.md) for the provider-specific parameters and requirements.

