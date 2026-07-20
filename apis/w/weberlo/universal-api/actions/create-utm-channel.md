# Weberlo: Create UTM Channel

Creates a UTM channel in Weberlo.

```
POST https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-utm-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-utm-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Branded UTM Channel",
  "icon": "https://example.com/utm-channel.png",
  "conditions[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-utm-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Branded UTM Channel",
    "icon": "https://example.com/utm-channel.png",
    "conditions[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | UTM channel name. Example: `Branded UTM Channel`. |
| `icon` | string | yes | UTM channel icon URL. Example: `https://example.com/utm-channel.png`. |
| `conditions[]` | array<object> | yes | UTM matching conditions array. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weberlo API returns.

## Native endpoint

Through the native Weberlo API, this operation is `POST /channel-utm` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-utm-channel.md) for the provider-specific parameters and requirements.

