# ZAP POST: List Submissions For Campaign

Retrieves submissions for a specific campaign from ZAP POST.

```
GET https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-submissions-for-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-submissions-for-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-submissions-for-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign UUID to list submissions for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZAP POST API returns.

## Native endpoint

Through the native ZAP POST API, this operation is `GET /api/v1/submissions/:campaignId` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions-for-campaign.md) for the provider-specific parameters and requirements.

