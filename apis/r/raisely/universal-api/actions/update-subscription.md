# Raisely: Update Subscription

Updates an existing subscription in Raisely.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.anonymous` | boolean | no | True if the person's name should be hidden from donation feeds Examples: `true`, `false` |
| `data.card` | string | no | The gateway card ID to charge when collecting the subscription Example: `card_aabbccddeeffaabbccddeeff` |
| `data.count` | number | no | The frequency of the subscription, used in conjunction with the `interval` property. For instance, a monthly subscription would have a `count` of `1` and an `interval` of `MONTH`. A fortnightly subscription would have a `count` of `2` and an `interval` of `WEEK`. Examples: `1`, `4` |
| `data.currency` | string | no | ISO alpha-3 letter currency code Examples: `AUD`, `USD` |
| `data.customer` | string | no | The gateway customer ID (only used when importing new subscriptions) Example: `cus_xxxxxxxxxxxxxx` |
| `data.email` | string | no | The user's email address. Raisely uses this as a unique identifier and will associate the subscription with an existing record if the email matches. Example: `harveymilk@example.com` |
| `data.firstName` | string | no | The first name of the person Example: `Leila` |
| `data.fullName` | string | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `data.interval` | string | no | The interval of the subscriptions. See `count`. Examples: `WEEK`, `MONTH`, `YEAR` |
| `data.items` | object<object> | no |  |
| `data.items[]..amount` | number | no | `public` The amount spent on the item in the currency of the donation |
| `data.items[]..amountRefunded` | number | no | `public` The total amount refunded in cents for this line item, in the donation currency. |
| `data.items[]..attendance` | string | no | `public` Whether the donation item (ticket) has been checked in |
| `data.items[]..campaignAmount` | number | no | `public` The amount spent on the item in the currency of the campaign |
| `data.items[]..createdAt` | string | no | `public` ISO8601 created timestamp |
| `data.items[]..description` | string | no | `public` Description of the item |
| `data.items[]..includeInTotals` | boolean | no | `public` If false, the amount is not included in receipts as part of the total donation |
| `data.items[]..itemId` | string | no | `public` The item ID / reference |
| `data.items[]..originalAmount` | number | no | `public` The total amount of this line item in cents prior to any refunds, in the donation currency. Amount is tax inclusive. |
| `data.items[]..parentBundleItem` | string | no | `public` The item ID / reference of this ticket's parent bundle |
| `data.items[]..parentBundleItemDescription` | string | no | `public` The ticket's parent bundle description |
| `data.items[]..perkUuid` | string | no | `public` Deprecated |
| `data.items[]..productUuid` | string | no | `public` The uuid for the associated product or ticket. |
| `data.items[]..quantity` | number | no | `public` If multiple of the item, the number of items claimed |
| `data.items[]..status` | string | no | `public` The status of the donation item |
| `data.items[]..type` | string | no | `public` The item type. For most manual API calls, you should use the value `OTHER`. |
| `data.items[]..updatedAt` | string | no | `public` ISO8601 created timestamp |
| `data.items[]..uuid` | string | no | `public` Unique identifier for the item |
| `data.lastName` | string | no | The last name of the person Example: `de Lima` |
| `data.message` | string | no | A public message left by the donor Example: `Glad to help out with the fundraising!` |
| `data.method` | string | no | The payment gateway used for the subscription. Use STRIPE_INTENT for new subscriptions. Examples: `STRIPE_INTENT`, `CREDIT_CARD`, `CUSTOM`, `PAYPAL` |
| `data.methodType` | string | no | The type of payment method used, to distinguish between card, direct debit and digital wallet payments. Examples: `CARD`, `APPLE_PAY`, `GOOGLE_PAY`, `BROWSER_PAY`, `DD_BACS`, `DD_BECS` |
| `data.nextPayment` | string | no | An ISO8601 timestamp of the next payment due date. Raisely will charge the donation after this date. Example: `2020-12-03T06:52:46.330Z` |
| `data.preferredDay` | number | no | Stores the preferred day for the subscription to be billed on. If interval is WEEK, it's day of the week. If interval is MONTH, it's the day of the month. If interval is YEAR, it's day of the year. Example: `12345` |
| `data.preferredName` | string | no | The name that the person prefers to be called Example: `Norma` |
| `data.private` | object | no | Private values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.public` | object | no | Public values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.source` | string | no | The source of this subscription. Subscriptions created through the API should have a source of `OFFLINE`. Examples: `OFFLINE`, `ONLINE` |
| `data.token` | string | no | Payment gateway token. Set to `null` when adding offline subscriptions with `card` and `customer`. Examples: `seti_xxxxxxxxxxxxxxxxxx`, `EXISTING_CARD` |
| `data.treatAsNewSubscription` | boolean | no | This field is only for importing new subscriptions. When false (default), the first successful charge of the card will result in a subscription.rebilled event. Set to true to change the first event to subscription.succeeded and send the Regular Donation Welcome message on the first payment after import. Examples: `true`, `false` |
| `overwriteCustomFields` | boolean | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "campaignUuid": "string",
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "failed": true,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "interval": "string",
      "lastName": "Chen",
      "method": "string",
      "mode": "string",
      "nextPayment": "2026-05-07T12:00:00.000Z",
      "profileUuid": "string",
      "source": "string",
      "status": "string",
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `campaignUuid` | string |  |
| `count` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `failed` | boolean |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `interval` | string |  |
| `lastName` | string |  |
| `method` | string |  |
| `mode` | string |  |
| `nextPayment` | date |  |
| `profileUuid` | string |  |
| `source` | string |  |
| `status` | string |  |
| `total` | number |  |
| `updatedAt` | date |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `PATCH /subscriptions/:uuid` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

