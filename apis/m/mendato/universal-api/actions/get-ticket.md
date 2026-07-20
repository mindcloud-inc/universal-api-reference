# Mendato: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-ticket?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-ticket?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato ticket query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ticket": {
        "completedAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "inputChannel": "string",
        "isPublic": true,
        "location": "string",
        "number": 1,
        "priority": "string",
        "rejectedAt": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ticket.completedAt` | date |  |
| `ticket.createdAt` | date |  |
| `ticket.description` | string |  |
| `ticket.dueDate` | date |  |
| `ticket.id` | string |  |
| `ticket.inputChannel` | string |  |
| `ticket.isPublic` | boolean |  |
| `ticket.location` | string |  |
| `ticket.number` | number |  |
| `ticket.priority` | string |  |
| `ticket.rejectedAt` | date |  |
| `ticket.status` | string |  |
| `ticket.type` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

