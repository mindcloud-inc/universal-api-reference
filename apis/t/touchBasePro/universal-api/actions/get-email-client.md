# TouchBasePro: Get Email Client

Retrieves an email client from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "basicDetails": {
        "clientId": "string",
        "companyName": "Ava Chen",
        "country": "string",
        "primaryContactEmail": "ava@example.com",
        "primaryContactName": "Ava Chen",
        "timeZone": "string"
      },
      "billingDetails": {
        "baseDeliveryRate": 1,
        "baseDesignSpamTestRate": 1,
        "baseRatePerRecipient": 1,
        "canPurchaseCredits": true,
        "clientPays": true,
        "credits": 1,
        "currency": "string",
        "markupOnDelivery": 1,
        "markupOnDesignSpamTest": 1,
        "markupPerRecipient": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `basicDetails.clientId` | string |  |
| `basicDetails.companyName` | string |  |
| `basicDetails.country` | string |  |
| `basicDetails.primaryContactEmail` | string |  |
| `basicDetails.primaryContactName` | string |  |
| `basicDetails.timeZone` | string |  |
| `billingDetails.baseDeliveryRate` | number |  |
| `billingDetails.baseDesignSpamTestRate` | number |  |
| `billingDetails.baseRatePerRecipient` | number |  |
| `billingDetails.canPurchaseCredits` | boolean |  |
| `billingDetails.clientPays` | boolean |  |
| `billingDetails.credits` | number |  |
| `billingDetails.currency` | string |  |
| `billingDetails.markupOnDelivery` | number |  |
| `billingDetails.markupOnDesignSpamTest` | number |  |
| `billingDetails.markupPerRecipient` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/clients` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-client.md) for the provider-specific parameters and requirements.

