# Buy Me a Coffee: Get Member

Retrieves a member from Buy Me a Coffee by membership ID.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-member?connectionId=$CONNECTION_ID&id=7979" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7979"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-member?${params}`, {
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
| `id` | number | yes | The unique ID of the membership returned by the list memberships action. Example: `7979`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "messageVisibility": 1,
      "payerEmail": "ava@example.com",
      "payerName": "Ava Chen",
      "referer": "string",
      "subscriptionCancelledOn": "2026-05-07T12:00:00.000Z",
      "subscriptionCoffeeNum": 1,
      "subscriptionCoffeePrice": "string",
      "subscriptionCreatedOn": "2026-05-07T12:00:00.000Z",
      "subscriptionCurrency": "string",
      "subscriptionCurrentPeriodEnd": "2026-05-07T12:00:00.000Z",
      "subscriptionCurrentPeriodStart": "2026-05-07T12:00:00.000Z",
      "subscriptionDurationType": "string",
      "subscriptionId": 1,
      "subscriptionIsCancelled": true,
      "subscriptionIsCancelledAtPeriodEnd": true,
      "subscriptionMessage": "string",
      "subscriptionUpdatedOn": "2026-05-07T12:00:00.000Z",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `messageVisibility` | number |  |
| `payerEmail` | string |  |
| `payerName` | string |  |
| `referer` | string |  |
| `subscriptionCancelledOn` | date |  |
| `subscriptionCoffeeNum` | number |  |
| `subscriptionCoffeePrice` | string |  |
| `subscriptionCreatedOn` | date |  |
| `subscriptionCurrency` | string |  |
| `subscriptionCurrentPeriodEnd` | date |  |
| `subscriptionCurrentPeriodStart` | date |  |
| `subscriptionDurationType` | string |  |
| `subscriptionId` | number |  |
| `subscriptionIsCancelled` | boolean |  |
| `subscriptionIsCancelledAtPeriodEnd` | boolean |  |
| `subscriptionMessage` | string |  |
| `subscriptionUpdatedOn` | date |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Buy Me a Coffee API, this operation is `GET /subscriptions/:id` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

