# WaiverFile: Update Event Category

Updates an existing event category in WaiverFile.

```
PUT https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventCategoryID": "string",
  "name": "Ava Chen",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventCategoryID": "string",
    "name": "Ava Chen",
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventCategoryID` | string | yes |  |
| `name` | string | yes |  |
| `active` | boolean | yes |  |

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

Through the native WaiverFile API, this operation is `POST /UpdateEventCategory` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-category.md) for the provider-specific parameters and requirements.

