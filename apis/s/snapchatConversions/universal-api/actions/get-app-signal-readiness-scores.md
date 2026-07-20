# Snapchat Conversions: Get App Signal Readiness Scores

Retrieves app signal readiness scores in Snapchat Conversions.

```
GET https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores?connectionId=$CONNECTION_ID&snapAppId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "snapAppId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores?${params}`, {
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
| `snapAppId` | string | yes | The Snapchat mobile app ID to retrieve event quality scores for. |
| `locale` | string | no | Optional locale code for the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snapchat Conversions API returns.

## Native endpoint

Through the native Snapchat Conversions API, this operation is `GET /mobile_apps/:snapAppId/event_quality_scores` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-signal-readiness-scores.md) for the provider-specific parameters and requirements.

