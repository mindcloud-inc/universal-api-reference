# Yutori: Update Scout Email Settings

Updates email settings and subscribers for a scout in Yutori.

```
PUT https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout-email-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout-email-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout-email-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scoutId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scoutId` | string | yes | The scout UUID. |
| `skipEmail` | boolean | no |  |
| `subscribersToAdd[]` | array<string> | no |  |
| `subscribersToRemove[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yutori API returns.

## Native endpoint

Through the native Yutori API, this operation is `PUT /v1/scouting/tasks/:scout_id/email-settings` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scout-email-settings.md) for the provider-specific parameters and requirements.

