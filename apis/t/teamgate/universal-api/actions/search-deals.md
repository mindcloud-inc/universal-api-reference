# Teamgate: Search Deals

Finds deals in Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/search-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/search-deals?connectionId=$CONNECTION_ID&limit=25&offset=0&nameLike=%25Codex%25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "nameLike": "%Codex%"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/search-deals?${params}`, {
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
| `nameLike` | string | yes | Substring match for the deal name. Use Teamgate % wildcards when needed, for example %Codex%. Example: `%Codex%`. |
| `source` | string | no | Deal source name filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `operator` | string | no | Logical operator for combining search conditions, such as OR. |
| `fields` | string | no | Comma-separated fields to return in the search response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": {},
      "created": {},
      "estimatedClosureDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "pipeline": {},
      "price": {},
      "source": {},
      "stage": {},
      "starred": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | object |  |
| `created` | object |  |
| `estimatedClosureDate` | date |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `pipeline` | object |  |
| `price` | object |  |
| `source` | object |  |
| `stage` | object |  |
| `starred` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /deals` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-deals.md) for the provider-specific parameters and requirements.

