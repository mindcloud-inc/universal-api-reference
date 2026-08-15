# Google Ads: Create Ad Group

Creates an ad group in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-ad-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-ad-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[].create.name": "Ava Chen",
  "operations[]": [
    "string"
  ],
  "operations[].create.campaign": "customers/1234567890/campaigns/9876543210"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-ad-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[].create.name": "Ava Chen",
    "operations[]": ["string"],
    "operations[].create.campaign": "customers/1234567890/campaigns/9876543210"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID where the ad group will be created (without dashes). Example: `1234567890`. |
| `operations[].create` | object | no |  |
| `operations[].create.name` | string | yes |  |
| `operations[]` | array | yes |  |
| `operations[].create.campaign` | string | yes | Campaign resource name for the ad group, format customers/{customer_id}/campaigns/{campaign_id}. Example: `customers/1234567890/campaigns/9876543210`. |
| `operations[].create.status` | string | no | Example: `ENABLED, PAUSED`. |
| `operations[].create.cpcBidMicros` | number | no | Example: `1000000`. |
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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/adGroups:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ad-group.md) for the provider-specific parameters and requirements.

