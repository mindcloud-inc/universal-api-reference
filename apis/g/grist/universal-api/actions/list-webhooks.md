# Grist: List Webhooks

Finds webhooks in a Grist document.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-webhooks?${params}`, {
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
| `docId` | string | yes | Document ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhooks": [
        {
          "fields": {
            "authorization": "string",
            "enabled": true,
            "eventTypes": [
              "string"
            ],
            "isReadyColumn": {},
            "memo": "string",
            "name": "Ava Chen",
            "tableId": "string",
            "unsubscribeKey": "string",
            "url": "https://example.com"
          },
          "id": "string",
          "usage": {
            "lastEventBatch": {},
            "numWaiting": 1,
            "status": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhooks[].fields.authorization` | string |  |
| `webhooks[].fields.enabled` | boolean |  |
| `webhooks[].fields.eventTypes[]` | string |  |
| `webhooks[].fields.isReadyColumn` | object |  |
| `webhooks[].fields.memo` | string |  |
| `webhooks[].fields.name` | string |  |
| `webhooks[].fields.tableId` | string |  |
| `webhooks[].fields.unsubscribeKey` | string |  |
| `webhooks[].fields.url` | string |  |
| `webhooks[].id` | string |  |
| `webhooks[].usage.lastEventBatch` | object |  |
| `webhooks[].usage.numWaiting` | number |  |
| `webhooks[].usage.status` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /docs/:docId/webhooks` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

