# Raklet: Get Donation



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-donation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-donation?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Raklet API, this operation is `GET /organisations/:organisationId/donations/:id` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-donation.md) for the provider-specific parameters and requirements.

