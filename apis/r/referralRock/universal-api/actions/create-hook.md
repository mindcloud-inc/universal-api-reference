# Referral Rock: Create Hook

Creates a webhook subscription in Referral Rock.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | The URL to call when the subscribed event occurs. |
| `event` | string | yes | The Referral Rock event to subscribe to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "web_hook_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `web_hook_id` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/hooks` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hook.md) for the provider-specific parameters and requirements.

