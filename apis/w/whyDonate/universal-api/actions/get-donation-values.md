# WhyDonate: Get Donation Values



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-donation-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-donation-values?connectionId=$CONNECTION_ID&slug=save-the-children&currency=eur" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "save-the-children",
  "currency": "eur"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-donation-values?${params}`, {
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
| `slug` | string | yes | Fundraiser slug used to fetch donation values. Example: `save-the-children`. |
| `currency` | string | yes | Explicit fundraiser currency code, for example eur. Runtime validation showed the endpoint succeeds with eur and fails with the old def fallback. Example: `eur`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "customdonationconfiguration": {
        "maxDonationAmount": "string",
        "minDonationAmount": "string",
        "primaryColor": "string"
      },
      "fundraiserData": {
        "amountTarget": 1,
        "id": 1,
        "isDraft": true,
        "slug": "string",
        "title": "string"
      },
      "symbol": "string",
      "tipAmount": {
        "defaultValues": {
          "tipAmountFixedDefault": 1,
          "tipAmountPercentageDefault": 1
        }
      },
      "xToEur": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `customdonationconfiguration.maxDonationAmount` | string |  |
| `customdonationconfiguration.minDonationAmount` | string |  |
| `customdonationconfiguration.primaryColor` | string |  |
| `fundraiserData.amountTarget` | number |  |
| `fundraiserData.id` | number |  |
| `fundraiserData.isDraft` | boolean |  |
| `fundraiserData.slug` | string |  |
| `fundraiserData.title` | string |  |
| `symbol` | string |  |
| `tipAmount.defaultValues.tipAmountFixedDefault` | number |  |
| `tipAmount.defaultValues.tipAmountPercentageDefault` | number |  |
| `xToEur` | string |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/donation/values` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-donation-values.md) for the provider-specific parameters and requirements.

