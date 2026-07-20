# Raisely: Update Donation

Updates an existing donation in Raisely.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-donation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | The `uuid` of the record |
| `data` | object | no |  |
| `data.anonymous` | boolean | no | Does the donor wish to be anonymous Examples: `true`, `false` |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.email` | string | no | Email address of the donor Example: `null` |
| `data.firstName` | string | no | (deprecated, use preferredName) Example: `null` |
| `data.fullName` | string | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `data.lastName` | string | no | Last name of the donor Example: `null` |
| `data.thankyou` | object | no |  |
| `data.thankyou.message` | string | no | Message to the donor from the fundraiser Example: `Thank you for your donation!` |
| `data.thankyou.isPrivate` | boolean | no | Does the fundraiser want the message to be private Examples: `true`, `false` |
| `data.preferredName` | string | no | The name that the person prefers to be called Example: `Norma` |
| `data.private` | object | no | Private values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.public` | object | no | Public values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.public.currency_symbol` | string | no | Currency symbol |
| `data.public.donation_amount` | string | no | Amount donated in dollars |
| `data.public.fee` | string | no | The fee paid on the donation in dollars |
| `data.public.fixed_amount` | string | no |  |
| `data.public.fixed_description` | string | no |  |
| `data.public.photo_url` | string | no | Donor photo url |

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

Through the native Raisely API, this operation is `PATCH /donations/:uuid` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-donation.md) for the provider-specific parameters and requirements.

