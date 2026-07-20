# LOBSTR.IO: List Runs

Retrieves runs from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&squid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "squid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-runs?${params}`, {
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
| `squid` | string | yes | The squid hash ID to list runs for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "limit": 1,
      "page": 1,
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | number |  |
| `page` | number |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/runs` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-runs.md) for the provider-specific parameters and requirements.

