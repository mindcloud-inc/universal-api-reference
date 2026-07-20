# Snapchat Conversions: Validate Test Events

Validates test conversion events in Snapchat Conversions.

```
GET https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/validate-test-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/validate-test-events?connectionId=$CONNECTION_ID&assetId=string&data%5B%5D=%5Bobject%20Object%5D&data%5B%5D.eventName=Ava%20Chen&data%5B%5D.eventTime=1&data%5B%5D.actionSource=string&data%5B%5D.eventSourceUrl=https%3A%2F%2Fexample.com&data%5B%5D.userData=%5Bobject%20Object%5D&data%5B%5D.userData.em%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string",
  "data[]": "[object Object]",
  "data[].eventName": "Ava Chen",
  "data[].eventTime": "1",
  "data[].actionSource": "string",
  "data[].eventSourceUrl": "https://example.com",
  "data[].userData": "[object Object]",
  "data[].userData.em[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/validate-test-events?${params}`, {
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
| `data[]` | array<object> | yes | Array of test conversion events to validate. |
| `data[].eventName` | string | yes | Snap conversion event name to validate. |
| `data[].eventTime` | number | yes | Epoch timestamp for the event, within the past seven days. |
| `data[].actionSource` | string | yes | Where the event took place. |
| `data[].eventSourceUrl` | string | yes | URL where the web event occurred. |
| `data[].userData` | object | yes | User matching fields for the event. |
| `data[].userData.em[]` | array<string> | yes | SHA-256 normalized email hashes for matching. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snapchat Conversions API returns.

## Native endpoint

Through the native Snapchat Conversions API, this operation is `POST https://tr.snapchat.com/v3/:asset_id/events/validate` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-test-events.md) for the provider-specific parameters and requirements.

