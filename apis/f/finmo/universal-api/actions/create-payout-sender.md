# Finmo: Create Payout Sender

Creates a new payout sender in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderName": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-sender', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderName": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderName` | string | yes |  |
| `type` | string | yes |  |
| `description` | string | no |  |
| `metadata` | object | no |  |
| `email` | string | no |  |
| `organizationReferenceId` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `addressCity` | string | no |  |
| `addressState` | string | no |  |
| `addressCountry` | string | no |  |
| `addressZipCode` | string | no |  |
| `phoneNumber` | string | no |  |
| `phoneCountryCode` | string | no |  |
| `phoneNumberE164` | string | no |  |
| `individual` | object | no |  |
| `company` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "individual": {},
      "isActive": true,
      "metadata": {},
      "orgId": "string",
      "payoutSenderId": "string",
      "senderName": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `individual` | object |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `orgId` | string |  |
| `payoutSenderId` | string |  |
| `senderName` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Finmo API, this operation is `POST /payout-sender` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout-sender.md) for the provider-specific parameters and requirements.

