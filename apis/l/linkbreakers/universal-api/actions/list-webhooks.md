# Linkbreakers: List Webhooks

Retrieves a list of webhooks from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-webhooks?${params}`, {
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
| `status` | string | no | Filter webhooks by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhooks": [
        {
          "createdAt": "string",
          "endpointUrl": "https://example.com",
          "failureCount": "string",
          "id": "string",
          "lastDeliveredAt": "string",
          "lastSentAt": "string",
          "linkId": "https://example.com",
          "name": "Ava Chen",
          "source": "string",
          "status": "string",
          "successCount": "string",
          "triggers": [
            "string"
          ],
          "updatedAt": "string",
          "workspaceId": "string"
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
| `webhooks` | array<object> | Webhooks in the workspace. |
| `webhooks[].createdAt` | string |  |
| `webhooks[].endpointUrl` | string |  |
| `webhooks[].failureCount` | string |  |
| `webhooks[].id` | string |  |
| `webhooks[].lastDeliveredAt` | string |  |
| `webhooks[].lastSentAt` | string |  |
| `webhooks[].linkId` | string |  |
| `webhooks[].name` | string |  |
| `webhooks[].source` | string |  |
| `webhooks[].status` | string |  |
| `webhooks[].successCount` | string |  |
| `webhooks[].triggers` | array<string> |  |
| `webhooks[].updatedAt` | string |  |
| `webhooks[].workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/webhooks` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

