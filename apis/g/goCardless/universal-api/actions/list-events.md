# GoCardless: List Events

Finds events in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-events?${params}`, {
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
| `action` | string | no |  |
| `billingRequest` | string | no |  |
| `createdAt` | object | no |  |
| `createdAt.gt` | date | no |  |
| `createdAt.gte` | date | no |  |
| `createdAt.lt` | date | no |  |
| `createdAt.lte` | date | no |  |
| `creditor` | string | no |  |
| `export` | string | no |  |
| `include` | string | no |  |
| `instalmentSchedule` | string | no |  |
| `mandate` | string | no |  |
| `outboundPayment` | string | no |  |
| `parentEvent` | string | no |  |
| `payerAuthorisation` | string | no |  |
| `payment` | string | no |  |
| `paymentAccountTransaction` | string | no |  |
| `payout` | string | no |  |
| `refund` | string | no |  |
| `resourceType` | string | no |  |
| `schemeIdentifier` | string | no |  |
| `subscription` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "action": "string",
          "createdAt": "string",
          "details": {
            "cause": "string",
            "description": "string",
            "origin": "string"
          },
          "id": "string",
          "links": {
            "payment": "https://example.com"
          },
          "resourceType": "string"
        }
      ],
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
| `events[].action` | string |  |
| `events[].createdAt` | string |  |
| `events[].details.cause` | string |  |
| `events[].details.description` | string |  |
| `events[].details.origin` | string |  |
| `events[].id` | string |  |
| `events[].links.payment` | string |  |
| `events[].resourceType` | string |  |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /events` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

