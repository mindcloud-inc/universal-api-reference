# Raisely: Create Donation

Creates a new donation in Raisely.

```
POST https://connect.mindcloud.co/v1/universal/raisely/latest/actions/create-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/create-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.currency": "string",
  "data.email": "ava@example.com",
  "data.method": "string",
  "data.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/create-donation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.currency": "string",
    "data.email": "ava@example.com",
    "data.method": "string",
    "data.type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no |  |
| `data.address1` | string | no | Line 1 of an address Example: `31 Sunset Boulevard` |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.address2` | string | no | Line 2 of an address Example: `Unit 31b` |
| `data.anonymous` | boolean | no | Does the donor wish to be anonymous Examples: `true`, `false` |
| `data.campaignUuid` | string | no | Unique identifier for the record Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `data.card` | string | no | ID of the payment method used (from the payment gateway) Example: `card_aabbccddeeffaabbccddeeff` |
| `data.country` | string | no | Examples: `AU`, `GB`, `US` |
| `data.currency` | string | yes | 3 letter currency code Examples: `AUD`, `USD` |
| `data.customer` | string | no | The customer ID (assigned by the payment gateway) |
| `data.date` | string | no | The date and time (in ISO8601 format) the donation was received by the organisation (only for OFFLINE donations) Example: `2020-12-03T06:52:46.330Z` |
| `data.email` | string | yes | Email address of the donor Example: `harveymilk@example.com` |
| `data.firstName` | string | no | The first name of the person Example: `Leila` |
| `data.forRegistration` | string | no | Not null values indicate this transaction has been set aside to pay for an upcoming registration Examples: `true`, `null` |
| `data.fullName` | string | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `data.gatewayVersion` | string | no | Gateway Version of donation method, if any |
| `data.items` | object<object> | no |  |
| `data.items[]..amount` | number | no | The amount spent on the item in the currency of the donation |
| `data.items[]..amountRefunded` | number | no | The total amount refunded in cents for this line item, in the donation currency. |
| `data.items[]..attendance` | string | no | Whether the donation item (ticket) has been checked in |
| `data.items[]..description` | string | no | Description of the item |
| `data.items[]..includeInTotals` | boolean | no | If false, the amount is not included in receipts as part of the total donation |
| `data.items[]..parentBundleItemDescription` | string | no | The ticket's parent bundle description |
| `data.items[]..quantity` | number | no | If multiple of the item, the number of items claimed |
| `data.lastName` | string | no | The last name of the person Example: `de Lima` |
| `data.message` | string | no | Message from the donor Example: `Glad to help out with the fundraising!` |
| `data.method` | string | yes | The payment gateway used Examples: `CREDIT_CARD`, `PAYPAL`, `APPLE_PAY`, `OFFLINE`, `CUSTOM`, `STRIPE_INTENT`, `FACEBOOK` |
| `data.methodType` | string | no | The type of payment method used, to distinguish between card, direct debit and digital wallet payments. Examples: `APPLE_PAY`, `CARD`, `GOOGLE_PAY`, `BROWSER_PAY` |
| `data.mode` | string | no | LIVE or TEST Examples: `LIVE`, `TEST` |
| `data.phoneNumber` | string | no | Phone number of the donor Example: `+1 123-456-7890` |
| `data.postcode` | string | no | Postal code of the donor Examples: `AAA BBBB`, `0000`, `AAA BBB` |
| `data.preferredName` | string | no | The name that the person prefers to be called Example: `Norma` |
| `data.private` | object | no | Private values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.profileUuid` | string | no | Unique identifier for the record Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `data.public` | object | no | Public values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.state` | string | no |  |
| `data.suburb` | string | no |  |
| `data.swiftAidStatus` | string | no | Status of donation on SwiftAid Examples: `OK`, `FAILED`, `PENDING`, `DELETING`, `DELETED` |
| `data.token` | string | no | The payment token from the gateway Example: `tok_aaaaaaaaaaaaaaaaaaaaaaaa` |
| `data.type` | string | yes | ONLINE or OFFLINE Examples: `ONLINE`, `OFFLINE` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "anonymous": true,
      "campaignUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "fee": 1,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "message": "string",
      "method": "string",
      "mode": "string",
      "preferredName": "Ava Chen",
      "profileUuid": "string",
      "publicAmount": 1,
      "publicFee": 1,
      "status": "string",
      "subscriptionUuid": "string",
      "total": 1,
      "type": "string",
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
| `anonymous` | boolean |  |
| `campaignUuid` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `fee` | number |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `message` | string |  |
| `method` | string |  |
| `mode` | string |  |
| `preferredName` | string |  |
| `profileUuid` | string |  |
| `publicAmount` | number |  |
| `publicFee` | number |  |
| `status` | string |  |
| `subscriptionUuid` | string |  |
| `total` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `POST /donations` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-donation.md) for the provider-specific parameters and requirements.

