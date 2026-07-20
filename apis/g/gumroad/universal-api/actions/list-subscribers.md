# Gumroad: List Subscribers

Retrieves subscribers for a Gumroad product.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-subscribers?${params}`, {
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
| `productId` | string | yes | The product ID. |
| `email` | string | no | Filter subscribers by this email. |
| `paginated` | boolean | no | Set to true to limit the response and return a next page key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageKey": "string",
      "nextPageUrl": "https://example.com",
      "subscribers": [
        [
          {}
        ]
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageKey` | string |  |
| `nextPageUrl` | string |  |
| `subscribers[]` | array<object> |  |
| `subscribers[].cancelledAt` | date |  |
| `subscribers[].chargeOccurrenceCount` | number |  |
| `subscribers[].createdAt` | date |  |
| `subscribers[].endedAt` | date |  |
| `subscribers[].failedAt` | date |  |
| `subscribers[].freeTrialEndsAt` | date |  |
| `subscribers[].id` | string |  |
| `subscribers[].licenseKey` | string |  |
| `subscribers[].productId` | string |  |
| `subscribers[].productName` | string |  |
| `subscribers[].purchaseIds[]` | array<string> |  |
| `subscribers[].recurrence` | string |  |
| `subscribers[].status` | string |  |
| `subscribers[].userEmail` | string |  |
| `subscribers[].userId` | string |  |
| `subscribers[].userRequestedCancellationAt` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /products/:product_id/subscribers` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

