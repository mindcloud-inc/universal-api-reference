# Kladana: List Contracts

Lists contracts in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-contracts?${params}`, {
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
      "agent": {},
      "archived": true,
      "code": "string",
      "contractType": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "moment": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "ownAgent": {},
      "shared": true,
      "state": {},
      "sum": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object | Counterparty reference. |
| `archived` | boolean | Whether the contract is archived. |
| `code` | string | Internal code. |
| `contractType` | string | Contract type. |
| `created` | date | Creation timestamp. |
| `description` | string | Contract description. |
| `externalCode` | string | External code. |
| `id` | string | Contract UUID. |
| `meta` | object | Kladana metadata reference. |
| `moment` | date | Contract date. |
| `name` | string | Contract name. |
| `ownAgent` | object | Own organization reference. |
| `shared` | boolean | Whether the contract is shared. |
| `state` | object | Contract state reference. |
| `sum` | number | Contract amount. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/contract` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

