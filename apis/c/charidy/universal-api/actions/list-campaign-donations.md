# Charidy: List Campaign Donations

Retrieves donations for a campaign from Charidy.

```
GET https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charidy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-donations?connectionId=$CONNECTION_ID&campaignId=96" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "96"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charidy/latest/actions/list-campaign-donations?${params}`, {
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
| `campaignId` | number | yes | The campaign ID whose donations to list. Example: `96`. |
| `sortBy` | string | no | Sort donations by the requested field and direction. Example: `-time`. |
| `limit` | number | no | Maximum number of donations to return. Example: `1`. |
| `fromDonationId` | number | no | Return donations made after this donation ID. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "campaignId": 1,
        "createdAt": 1,
        "currencyCode": "string",
        "currencySign": "string",
        "dedication": "string",
        "gatewayName": "Ava Chen",
        "hideDonationAmount": true,
        "name": "Ava Chen",
        "realPayment": 1,
        "teamId": 1,
        "total": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.campaignId` | number | Campaign ID. |
| `attributes.createdAt` | number | Donation creation timestamp. |
| `attributes.currencyCode` | string | Donation currency code. |
| `attributes.currencySign` | string | Donation currency sign. |
| `attributes.dedication` | string | Donation dedication text. |
| `attributes.gatewayName` | string | Gateway name. |
| `attributes.hideDonationAmount` | boolean | Whether the amount is hidden. |
| `attributes.name` | string | Donation display name. |
| `attributes.realPayment` | number | Real payment amount. |
| `attributes.teamId` | number | Associated team ID. |
| `attributes.total` | number | Total donation amount. |
| `id` | string | Unique donation ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Charidy API, this operation is `GET /api/v1/campaign/:campaignId/donations` (base URL `https://api.charidy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-donations.md) for the provider-specific parameters and requirements.

