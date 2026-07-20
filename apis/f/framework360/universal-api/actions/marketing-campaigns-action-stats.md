# Framework360: List Campaign Action Stats



```
GET https://connect.mindcloud.co/v1/universal/framework360/latest/actions/marketing-campaigns-action-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/marketing-campaigns-action-stats?connectionId=$CONNECTION_ID&campaignId=string&type=string&actionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "type": "string",
  "actionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/marketing-campaigns-action-stats?${params}`, {
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
| `campaignId` | string | yes | Marketing campaign ID. |
| `type` | string | yes | Campaign action type. |
| `actionId` | string | yes | Campaign action ID. |
| `page` | number | no | Results page number. |
| `limit` | number | no | Maximum number of results per page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `GET marketing/campaigns/action/stats` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/marketing-campaigns-action-stats.md) for the provider-specific parameters and requirements.

