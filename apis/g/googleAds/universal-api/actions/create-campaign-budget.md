# Google Ads: Create Campaign Budget

Creates a campaign budget in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[].create.deliveryMethod": "string",
  "operations[].create.amountMicros": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[].create.deliveryMethod": "string",
    "operations[].create.amountMicros": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID where the campaign budget will be created (without dashes). Example: `1234567890`. |
| `operations[].create` | object | no |  |
| `operations[].create.name` | string | no |  |
| `operations[]` | array | no |  |
| `operations[].create.deliveryMethod` | list | yes |  |
| `operations[].create.amountMicros` | number | yes |  |
| `operations[].create.operationsCreatePeriod` | string | no |  |
| `operations[].create.operationsCreateStartDate` | string | no |  |
| `operations[].create.operationsCreateEndDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/campaignBudgets:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-budget.md) for the provider-specific parameters and requirements.

