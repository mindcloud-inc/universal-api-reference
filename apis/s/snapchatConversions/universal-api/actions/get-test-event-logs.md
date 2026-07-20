# Snapchat Conversions: Get Test Event Logs

Retrieves test event logs in Snapchat Conversions.

```
GET https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-test-event-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-test-event-logs?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-test-event-logs?${params}`, {
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
| `assetId` | string | yes | Valid Snapchat Pixel ID or Snap App ID associated with the token. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snapchat Conversions API returns.

## Native endpoint

Through the native Snapchat Conversions API, this operation is `GET https://tr.snapchat.com/v3/:asset_id/events/validate/logs` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-event-logs.md) for the provider-specific parameters and requirements.

