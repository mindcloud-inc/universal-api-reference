# Gumroad: List Payouts

Retrieves payouts from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-payouts?${params}`, {
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
| `after` | date | no | Only return payouts after this date (YYYY-MM-DD). |
| `before` | date | no | Only return payouts before this date (YYYY-MM-DD). |
| `includeUpcoming` | boolean | no | Set to false to exclude upcoming payouts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageKey": "string",
      "nextPageUrl": "https://example.com",
      "payouts": [
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
| `payouts[]` | array<object> |  |
| `payouts[].amount` | string |  |
| `payouts[].bankAccountVisual` | string |  |
| `payouts[].createdAt` | date |  |
| `payouts[].currency` | string |  |
| `payouts[].id` | string |  |
| `payouts[].paymentProcessor` | string |  |
| `payouts[].paypalEmail` | string |  |
| `payouts[].processedAt` | date |  |
| `payouts[].status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /payouts` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payouts.md) for the provider-specific parameters and requirements.

