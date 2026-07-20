# Quo: List Webhooks

Retrieves all webhooks from Quo.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-webhooks?${params}`, {
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
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": {},
      "events": [
        "string"
      ],
      "id": "string",
      "key": "string",
      "label": "string",
      "orgId": "string",
      "resourceIds": [
        "string"
      ],
      "status": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `events[]` | string |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `orgId` | string |  |
| `resourceIds[]` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /webhooks` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

