# Loopy Loyalty: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignName": "Spring Coffee Rewards",
  "description": "Collect stamps for every purchase.",
  "organisationName": "MindCloud Coffee",
  "businessAddressLine1": "113 Concord Road",
  "businessCity": "Wayland",
  "businessCountry": "US",
  "businessEmail": "rewards@example.com",
  "businessStateProvinceRegion": "MA",
  "businessWebsite": "https://mindcloud.co",
  "collectValue": "Buy one coffee to get 1 stamp.",
  "rewardName": "Free Coffee",
  "rewardText": "Get a free coffee after collecting 10 stamps.",
  "stampsRequired": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignName": "Spring Coffee Rewards",
    "description": "Collect stamps for every purchase.",
    "organisationName": "MindCloud Coffee",
    "businessAddressLine1": "113 Concord Road",
    "businessCity": "Wayland",
    "businessCountry": "US",
    "businessEmail": "rewards@example.com",
    "businessStateProvinceRegion": "MA",
    "businessWebsite": "https://mindcloud.co",
    "collectValue": "Buy one coffee to get 1 stamp.",
    "rewardName": "Free Coffee",
    "rewardText": "Get a free coffee after collecting 10 stamps.",
    "stampsRequired": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignName` | string | yes | Name of the campaign to create. Example: `Spring Coffee Rewards`. |
| `description` | string | yes | Description for the campaign. Example: `Collect stamps for every purchase.`. |
| `organisationName` | string | yes | Organisation name shown on the campaign. Example: `MindCloud Coffee`. |
| `businessAddressLine1` | string | yes | Primary street address for the business. Example: `113 Concord Road`. |
| `businessCity` | string | yes | City for the business address. Example: `Wayland`. |
| `businessCountry` | string | yes | Two-letter country code for the business. Example: `US`. |
| `businessEmail` | string | yes | Contact email for the business. Example: `rewards@example.com`. |
| `businessStateProvinceRegion` | string | yes | State, province, or region for the business. Example: `MA`. |
| `businessWebsite` | string | yes | Website URL for the business. Example: `https://mindcloud.co`. |
| `collectValue` | string | yes | What the customer must do to collect one stamp. Example: `Buy one coffee to get 1 stamp.`. |
| `rewardName` | string | yes | Name of the reward customers earn. Example: `Free Coffee`. |
| `rewardText` | string | yes | Description of the reward customers earn. Example: `Get a free coffee after collecting 10 stamps.`. |
| `stampsRequired` | number | yes | Number of stamps required to earn the reward. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "revision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created campaign ID. |
| `revision` | string | Revision token returned by Loopy Loyalty. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /campaign` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

