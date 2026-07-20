# Recurly: List Plans



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-plans?${params}`, {
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
| `beginTime` | string | no |  |
| `endTime` | string | no |  |
| `ids` | string | no |  |
| `state` | string | no | One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingCode": "string",
      "allowAnyItemOnSubscriptions": true,
      "autoRenew": true,
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencies": [
        {}
      ],
      "customFields": [
        {}
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dunningCampaignId": "string",
      "harmonizedSystemCode": "string",
      "hostedPages": {},
      "id": "string",
      "intervalLength": 1,
      "intervalUnit": "string",
      "name": "Ava Chen",
      "object": "string",
      "pricingModel": "string",
      "rampIntervals": [
        {}
      ],
      "revenueScheduleType": "string",
      "setupFeeAccountingCode": "string",
      "setupFeeRevenueScheduleType": "string",
      "setupFees": [
        {}
      ],
      "state": "string",
      "taxCode": "string",
      "taxExempt": true,
      "totalBillingCycles": 1,
      "trialLength": 1,
      "trialRequiresBillingInfo": true,
      "trialUnit": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingCode` | string |  |
| `allowAnyItemOnSubscriptions` | boolean |  |
| `autoRenew` | boolean |  |
| `code` | string |  |
| `createdAt` | date |  |
| `currencies` | array<object> |  |
| `customFields` | array<object> |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `dunningCampaignId` | string |  |
| `harmonizedSystemCode` | string |  |
| `hostedPages` | object |  |
| `id` | string |  |
| `intervalLength` | number |  |
| `intervalUnit` | string |  |
| `name` | string |  |
| `object` | string |  |
| `pricingModel` | string |  |
| `rampIntervals` | array<object> |  |
| `revenueScheduleType` | string |  |
| `setupFeeAccountingCode` | string |  |
| `setupFeeRevenueScheduleType` | string |  |
| `setupFees` | array<object> |  |
| `state` | string |  |
| `taxCode` | string |  |
| `taxExempt` | boolean |  |
| `totalBillingCycles` | number |  |
| `trialLength` | number |  |
| `trialRequiresBillingInfo` | boolean |  |
| `trialUnit` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /plans` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

