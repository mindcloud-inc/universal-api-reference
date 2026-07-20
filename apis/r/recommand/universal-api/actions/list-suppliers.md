# Recommand: List Suppliers

Retrieves supplier records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-suppliers?${params}`, {
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
| `search` | string | no | search parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1,
        "totalPages": 1
      },
      "success": true,
      "suppliers": [
        {
          "createdAt": "string",
          "externalId": "string",
          "id": "string",
          "labels": [
            {}
          ],
          "name": "Ava Chen",
          "peppolAddresses": [
            "string"
          ],
          "teamId": "string",
          "updatedAt": "string",
          "vatNumber": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `success` | boolean |  |
| `suppliers` | array<object> |  |
| `suppliers[].createdAt` | string |  |
| `suppliers[].externalId` | string |  |
| `suppliers[].id` | string |  |
| `suppliers[].labels` | array<object> |  |
| `suppliers[].name` | string |  |
| `suppliers[].peppolAddresses` | array<string> |  |
| `suppliers[].teamId` | string |  |
| `suppliers[].updatedAt` | string |  |
| `suppliers[].vatNumber` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/suppliers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

