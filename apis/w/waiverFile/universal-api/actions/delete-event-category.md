# WaiverFile: Delete Event Category

Deletes an existing event category from WaiverFile.

```
DELETE https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/delete-event-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/delete-event-category?connectionId=$CONNECTION_ID&eventCategoryID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventCategoryID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/delete-event-category?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventCategoryID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `_WPObjectStatus` | number |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `POST /DeleteEventCategory` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event-category.md) for the provider-specific parameters and requirements.

