# GoCardless: List Refunds

Finds refunds in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-refunds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-refunds?${params}`, {
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
| `createdAt` | object | no |  |
| `createdAt.gt` | date | no |  |
| `createdAt.gte` | date | no |  |
| `createdAt.lt` | date | no |  |
| `createdAt.lte` | date | no |  |
| `mandate` | string | no |  |
| `payment` | string | no |  |
| `refundType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "cursors": {
          "after": {},
          "before": {}
        },
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /refunds` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-refunds.md) for the provider-specific parameters and requirements.

