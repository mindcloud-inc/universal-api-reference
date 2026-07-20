# OpenSanctions: List Entity Statements



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-entity-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-entity-statements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-entity-statements?${params}`, {
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
| `entity_id` | string | no | Filter statements by source entity ID. Default: `Q7747`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "total": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of statements requested. |
| `offset` | number | Offset of the statement results. |
| `results` | array<object> | Statement records. |
| `total` | object | Total statement count metadata. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /statements` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entity-statements.md) for the provider-specific parameters and requirements.

