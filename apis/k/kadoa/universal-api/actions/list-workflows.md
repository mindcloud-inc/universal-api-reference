# Kadoa: List Workflows



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-workflows?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | Response format. Accepted values: json, csv. One of: `csv`, `json`. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "limit": 1,
        "page": 1,
        "totalCount": 1,
        "totalPages": 1
      },
      "workflows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.totalCount` | number |  |
| `pagination.totalPages` | number |  |
| `workflows` | array<object> |  |

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/workflows` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

