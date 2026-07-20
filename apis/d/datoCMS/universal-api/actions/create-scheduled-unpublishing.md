# DatoCMS: Create Scheduled Unpublishing



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-scheduled-unpublishing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-scheduled-unpublishing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "scheduledAt": "2026-03-10T12:00:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-scheduled-unpublishing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "scheduledAt": "2026-03-10T12:00:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | Record ID. |
| `scheduledAt` | date | yes | ISO-8601 datetime for unpublishing. Example: `2026-03-10T12:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "contentInLocales": "string",
        "unpublishingScheduledAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "item": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.contentInLocales` | string |  |
| `attributes.unpublishingScheduledAt` | date |  |
| `id` | string |  |
| `relationships.item.data.id` | string |  |
| `relationships.item.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /items/:itemId/scheduled-unpublishing` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduled-unpublishing.md) for the provider-specific parameters and requirements.

