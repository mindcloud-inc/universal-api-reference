# Yotpo Loyalty & Referrals: Get Active Campaigns

Retrieves active campaigns from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-campaigns?${params}`, {
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
| `withStatus` | boolean | no | Include status information when set to true. |
| `customerEmail` | string | no | Filter campaigns for a specific customer email. |
| `customerId` | string | no | Filter campaigns for a specific customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionName": "Ava Chen",
      "adminDisplayName": "Ava Chen",
      "askYear": true,
      "createdAt": "string",
      "ctaText": "string",
      "defaultEmailBody": "ava@example.com",
      "details": "string",
      "detailsWithMultiCurrencyTemplate": "string",
      "displayOrder": 1,
      "endsAt": "string",
      "entityId": "string",
      "excludeAudienceIds": "string",
      "excludeAudienceNames": "Ava Chen",
      "expiresAt": "string",
      "extraCopy1": "string",
      "extraCopy2": "string",
      "hashtags": "string",
      "icon": "string",
      "id": 1,
      "includeAudienceIds": "string",
      "includeAudienceNames": "Ava Chen",
      "maxCompletionsPerUser": 1,
      "minActionsRequired": 1,
      "question": "string",
      "rewardText": "string",
      "shareText": "string",
      "title": "string",
      "titleWithMultiCurrencyTemplate": "string",
      "type": "string",
      "unrenderedDetails": "string",
      "unrenderedTitle": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionName` | string |  |
| `adminDisplayName` | string |  |
| `askYear` | boolean |  |
| `createdAt` | string |  |
| `ctaText` | string |  |
| `defaultEmailBody` | string |  |
| `details` | string |  |
| `detailsWithMultiCurrencyTemplate` | string |  |
| `displayOrder` | number |  |
| `endsAt` | string |  |
| `entityId` | string |  |
| `excludeAudienceIds` | string |  |
| `excludeAudienceNames` | string |  |
| `expiresAt` | string |  |
| `extraCopy1` | string |  |
| `extraCopy2` | string |  |
| `hashtags` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `includeAudienceIds` | string |  |
| `includeAudienceNames` | string |  |
| `maxCompletionsPerUser` | number |  |
| `minActionsRequired` | number |  |
| `question` | string |  |
| `rewardText` | string |  |
| `shareText` | string |  |
| `title` | string |  |
| `titleWithMultiCurrencyTemplate` | string |  |
| `type` | string |  |
| `unrenderedDetails` | string |  |
| `unrenderedTitle` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/campaigns` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-campaigns.md) for the provider-specific parameters and requirements.

