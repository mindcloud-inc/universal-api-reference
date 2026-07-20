# GrassBlade LRS: Replace Agent Profile

Replaces an agent profile in GrassBlade LRS.

```
PUT https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/replace-agent-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/replace-agent-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agent": "[object Object]",
  "profileId": "mindcloud-agent-profile-stage3",
  "document": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/replace-agent-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agent": "[object Object]",
    "profileId": "mindcloud-agent-profile-stage3",
    "document": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent` | string | yes | Example: `[object Object]`. |
| `profileId` | string | yes | Example: `mindcloud-agent-profile-stage3`. |
| `document` | object | yes | Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `PUT /agents/profile` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-agent-profile.md) for the provider-specific parameters and requirements.

