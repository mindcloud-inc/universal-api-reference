# Atlas AI Revenue Engine: Detach Knowledge Base File from Campaign



```
DELETE https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/detach-knowledge-base-file-from-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlas AI Revenue Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/detach-knowledge-base-file-from-campaign?connectionId=$CONNECTION_ID&campaignId=string&rowKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "rowKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/detach-knowledge-base-file-from-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign ID. |
| `rowKey` | string | yes | The file row key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlas AI Revenue Engine API returns.

## Native endpoint

Through the native Atlas AI Revenue Engine API, this operation is `DELETE /knowledgebase/:campaignId/:rowKey` (base URL `https://api.youratlas.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-knowledge-base-file-from-campaign.md) for the provider-specific parameters and requirements.

