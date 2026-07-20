# Loopy Loyalty: Update Campaign



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "5fcDywPejwj9QszwngBTKg",
  "campaignName": "Codex Stage3 Campaign 2",
  "description": "Collect stamps for every purchase.",
  "organisationName": "MindCloud Coffee",
  "businessAddressLine1": "113 Concord Road",
  "businessCity": "Wayland",
  "businessCountry": "US",
  "businessEmail": "apps@mindcloud.co",
  "businessStateProvinceRegion": "MA",
  "businessWebsite": "https://mindcloud.co",
  "collectValue": "Buy one coffee to get 1 stamp.",
  "rewardName": "Free Coffee",
  "rewardText": "Get a free coffee after collecting 10 stamps.",
  "stampsRequired": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "5fcDywPejwj9QszwngBTKg",
    "campaignName": "Codex Stage3 Campaign 2",
    "description": "Collect stamps for every purchase.",
    "organisationName": "MindCloud Coffee",
    "businessAddressLine1": "113 Concord Road",
    "businessCity": "Wayland",
    "businessCountry": "US",
    "businessEmail": "apps@mindcloud.co",
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
| `id` | string | yes | Campaign ID to update. Example: `5fcDywPejwj9QszwngBTKg`. |
| `campaignName` | string | yes | Updated campaign name. Example: `Codex Stage3 Campaign 2`. |
| `description` | string | yes | Updated campaign description. Example: `Collect stamps for every purchase.`. |
| `organisationName` | string | yes | Organisation name shown on the campaign. Example: `MindCloud Coffee`. |
| `businessAddressLine1` | string | yes | Primary street address for the business. Example: `113 Concord Road`. |
| `businessCity` | string | yes | City for the business address. Example: `Wayland`. |
| `businessCountry` | string | yes | Two-letter country code for the business. Example: `US`. |
| `businessEmail` | string | yes | Contact email for the business. Example: `apps@mindcloud.co`. |
| `businessStateProvinceRegion` | string | yes | State, province, or region for the business. Example: `MA`. |
| `businessWebsite` | string | yes | Website URL for the business. Example: `https://mindcloud.co`. |
| `collectValue` | string | yes | Updated stamp collection rule. Example: `Buy one coffee to get 1 stamp.`. |
| `rewardName` | string | yes | Updated reward name. Example: `Free Coffee`. |
| `rewardText` | string | yes | Updated reward description. Example: `Get a free coffee after collecting 10 stamps.`. |
| `stampsRequired` | number | yes | Number of stamps required to earn the reward. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uniqueEmailFieldName` | string | no | Field name to enforce as the campaign's unique email identifier. Example: `Email Address`. |
| `uniquePhoneFieldName` | string | no | Field name to enforce as the campaign's unique phone identifier. Example: `Mobile Number`. |
| `status` | number | no | Campaign status: 1 for draft, 2 for published. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowPushToPasses": true,
      "business": {
        "name": "Ava Chen",
        "website": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "pkTemplateName": "Ava Chen",
      "status": 1,
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPushToPasses` | boolean | Whether push notifications are enabled. |
| `business.name` | string | Business name. |
| `business.website` | string | Business website. |
| `description` | string | Campaign description. |
| `id` | string | Campaign ID. |
| `name` | string | Campaign name. |
| `pkTemplateName` | string | Wallet template name. |
| `status` | number | Campaign status. |
| `updateTime` | string | Campaign updated timestamp. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `PATCH /campaign/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

