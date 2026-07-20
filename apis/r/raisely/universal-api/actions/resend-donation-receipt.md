# Raisely: Resend Donation Receipt

Resends a donation receipt from Raisely.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/resend-donation-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/resend-donation-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/resend-donation-receipt', {
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
| `data.email` | string | no | Optional email to send the receipt to (defaults to the email on the donation) |

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

Through the native Raisely API, this operation is `POST /donations/:uuid/resend` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-donation-receipt.md) for the provider-specific parameters and requirements.

