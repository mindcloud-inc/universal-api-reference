# MILKEE: List Proposals

Retrieves proposals from MILKEE.

```
GET https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/list-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/list-proposals?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=4640" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "4640"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/list-proposals?${params}`, {
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
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `GET /companies/:companyId/proposals` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-proposals.md) for the provider-specific parameters and requirements.

