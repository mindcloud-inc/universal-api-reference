# SuperSend: Get Capacity Summary

Retrieves the capacity summary from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-capacity-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-capacity-summary?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-capacity-summary?${params}`, {
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
| `teamId` | string | yes | Team UUID (from list teams) |
| `page` | number | no | Default: 1. |
| `limit` | number | no | Default: 20. |
| `sortBy` | string | no | Default: projectedCompletionDays. |
| `sortDirection` | string | no | Allowed values: asc, desc. Default: asc. |
| `planningFilter` | string | no | Allowed values: all, active, inactive, finished, no-capacity. Default: all. |
| `search` | string | no |  |
| `includeCampaignId` | string | no | When set, response includes focusedCampaign with this campaign's row even if it would not appear on the requested page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        [
          {}
        ]
      ],
      "completionForecastChart": [
        [
          {}
        ]
      ],
      "overview": {},
      "pagination": {},
      "recommendations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns[]` | array<object> |  |
| `completionForecastChart[]` | array<object> |  |
| `overview` | object |  |
| `pagination` | object |  |
| `recommendations` | object |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /intelligence/capacity-summary` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-capacity-summary.md) for the provider-specific parameters and requirements.

