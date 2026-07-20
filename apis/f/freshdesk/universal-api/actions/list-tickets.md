# Freshdesk: List Tickets

Retrieves a list of tickets from Freshdesk.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-tickets?${params}`, {
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
| `filter` | list<string> | no | Predefined Freshdesk ticket filter (new_and_my_open, watching, spam, deleted). One of: `deleted`, `new_and_my_open`, `spam`, `watching`. |
| `include` | string | no | Embed additional fields (stats, requester, description). |

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

Through the native Freshdesk API, this operation is `GET /tickets` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

