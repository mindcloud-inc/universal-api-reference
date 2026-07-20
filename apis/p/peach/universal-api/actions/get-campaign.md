# Peach: Get Campaign

Retrieves a campaign from Peach.

```
GET https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | The unique identifier of the campaign to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "campaignGoal": "string",
      "campaignId": "string",
      "currency": {
        "en": "string",
        "he": "string"
      },
      "currencyOptions": [
        "string"
      ],
      "customProperties": [
        {
          "ref": "string",
          "required": true,
          "type": "string"
        }
      ],
      "displayDonations": true,
      "displayGraphicsAbout": true,
      "displayGroups": true,
      "enableInstallments": true,
      "hideButtons": true,
      "internalName": "Ava Chen",
      "isProductGoal": true,
      "name": {
        "en": "Ava Chen",
        "he": "Ava Chen"
      },
      "paymentMethods": [
        "string"
      ],
      "paymentTemplate": "string",
      "productCost": "string",
      "showMoneyGoal": true,
      "supportedLanguages": [
        "string"
      ],
      "telForCustomers": "string",
      "type": "string",
      "updatedAt": 1,
      "urlId": "https://example.com",
      "vouchers": [
        {
          "active": true,
          "amount": "string"
        }
      ],
      "whatsappForCustomers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `campaignGoal` | string |  |
| `campaignId` | string |  |
| `currency` | object |  |
| `currency.en` | string |  |
| `currency.he` | string |  |
| `currencyOptions` | array<string> |  |
| `customProperties` | array<object> |  |
| `customProperties[].ref` | string |  |
| `customProperties[].required` | boolean |  |
| `customProperties[].type` | string |  |
| `displayDonations` | boolean |  |
| `displayGraphicsAbout` | boolean |  |
| `displayGroups` | boolean |  |
| `enableInstallments` | boolean |  |
| `hideButtons` | boolean |  |
| `internalName` | string |  |
| `isProductGoal` | boolean |  |
| `name` | object |  |
| `name.en` | string |  |
| `name.he` | string |  |
| `paymentMethods` | array<string> |  |
| `paymentTemplate` | string |  |
| `productCost` | string |  |
| `showMoneyGoal` | boolean |  |
| `supportedLanguages` | array<string> |  |
| `telForCustomers` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |
| `urlId` | string |  |
| `vouchers` | array<object> |  |
| `vouchers[].active` | boolean |  |
| `vouchers[].amount` | string |  |
| `whatsappForCustomers` | string |  |

## Native endpoint

Through the native Peach API, this operation is `GET /campaigns/:campaignId` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

