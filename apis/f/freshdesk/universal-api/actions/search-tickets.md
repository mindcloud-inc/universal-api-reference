# Freshdesk: Search Tickets

Finds tickets in Freshdesk by query.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/search-tickets?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/search-tickets?${params}`, {
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
| `query` | string | yes | Freshdesk filter query syntax, for example status:2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdAt": "string",
      "dueBy": "string",
      "frDueBy": "string",
      "id": 1,
      "priority": 1,
      "requesterId": 1,
      "source": 1,
      "status": 1,
      "subject": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdAt` | string |  |
| `dueBy` | string |  |
| `frDueBy` | string |  |
| `id` | number |  |
| `priority` | number |  |
| `requesterId` | number |  |
| `source` | number |  |
| `status` | number |  |
| `subject` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `GET /search/tickets` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

