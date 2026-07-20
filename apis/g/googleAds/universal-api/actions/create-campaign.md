# Google Ads: Create Campaign

Creates a campaign in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[].create.name": "Ava Chen",
  "operations[]": [
    {}
  ],
  "operations[].create.campaignBudget": "string",
  "operations[].create.advertisingChannelType": "SEARCH"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[].create.name": "Ava Chen",
    "operations[]": [{}],
    "operations[].create.campaignBudget": "string",
    "operations[].create.advertisingChannelType": "SEARCH"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID where the campaign will be created (without dashes). Default: `4556174691`. Example: `1234567890`. |
| `operations[].create` | object | no |  |
| `operations[].create.manualCpc` | object | no |  |
| `operations[].create.name` | string | yes |  |
| `operations[].create.networkSettings.targetGoogleSearch` | boolean | no |  |
| `operations[]` | array<object> | yes |  |
| `operations[].create.campaignBudget` | string | yes |  |
| `operations[].create.networkSettings.targetSearchNetwork` | boolean | no |  |
| `operations[].create.advertisingChannelType` | list | yes | One of: `DISPLAY`, `PERFORMANCE_MAX`, `SEARCH`, `SHOPPING`, `VIDEO`. Default: `SEARCH`. |
| `operations[].create.networkSettings.targetContentNetwork` | boolean | no |  |
| `operations[].create.networkSettings.targetPartnerSearchNetwork` | boolean | no |  |
| `operations[].create.status` | list | no | One of: `ENABLED`, `PAUSED`. Default: `PAUSED`. |
| `operations[].create.networkSettings` | object | no |  |
| `operations[].create.containsEuPoliticalAdvertising` | list | no | One of: `CONTAINS_EU_POLITICAL_ADVERTISING`, `DOES_NOT_CONTAIN_EU_POLITICAL_ADVERTISING`, `UNKNOWN`, `UNSPECIFIED`. Default: `DOES_NOT_CONTAIN_EU_POLITICAL_ADVERTISING`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partialFailure` | boolean | no | Default: `false`. |
| `responseContentType` | list | no | One of: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. Default: `RESOURCE_NAME_ONLY`. |
| `validateOnly` | boolean | no | Default: `true`. |

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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/campaigns:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

