# Verix: List Credentials

Retrieves credentials from your Verix account.

```
GET https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-credentials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-credentials?${params}`, {
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
| `pageSize` | number | no | Number of credentials to return per page. Example: `10`. |
| `pageNumber` | number | no | 1-based page number to retrieve. Example: `1`. |
| `name` | string | no | Approximate credential name to search. Example: `Participation certificate`. |
| `groupId` | number | no | Filter credentials by Verix group ID. Example: `894`. |
| `externalId` | string | no | Filter credentials by recipient external ID. Example: `john_external_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": [
        {}
      ],
      "meta": {
        "currentPage": 1,
        "itemsPerPage": 1,
        "totalItems": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | array<object> | Credential records returned for the current page. |
| `meta` | object | Pagination metadata. |
| `meta.currentPage` | number | Current page number. |
| `meta.itemsPerPage` | number | Items returned per page. |
| `meta.totalItems` | number | Total matching credentials. |
| `meta.totalPages` | number | Total available pages. |

## Native endpoint

Through the native Verix API, this operation is `GET /v1/credentials` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

