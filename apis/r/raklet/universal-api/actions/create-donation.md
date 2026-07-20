# Raklet: Create Donation



```
POST https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-donation', {
  method: 'POST',
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
| `organisationMembershipId` | string | no |  |
| `amount` | number | no |  |
| `paymentMethod` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": 1,
      "donationCampaignId": "string",
      "fullName": "Ava Chen",
      "id": "string",
      "isDonorNameHidden": true,
      "isManualPayment": true,
      "isPublicDonation": true,
      "isRecurring": true,
      "organisationMembershipId": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": 1,
      "referenceNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdOn` | date |  |
| `currency` | number |  |
| `donationCampaignId` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isDonorNameHidden` | boolean |  |
| `isManualPayment` | boolean |  |
| `isPublicDonation` | boolean |  |
| `isRecurring` | boolean |  |
| `organisationMembershipId` | string |  |
| `paymentDate` | date |  |
| `paymentMethod` | number |  |
| `referenceNumber` | string |  |

## Native endpoint

Through the native Raklet API, this operation is `POST /organisations/:organisationId/donations` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-donation.md) for the provider-specific parameters and requirements.

