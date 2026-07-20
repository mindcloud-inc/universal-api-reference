# Mux: Update User Agent Restriction



```
PUT https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-user-agent-restriction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-user-agent-restriction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowHighRiskUserAgent": true,
  "allowNoUserAgent": true,
  "playbackRestrictionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-user-agent-restriction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowHighRiskUserAgent": true,
    "allowNoUserAgent": true,
    "playbackRestrictionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowHighRiskUserAgent` | boolean | yes | Whether high-risk user agents are allowed. |
| `allowNoUserAgent` | boolean | yes | Whether requests without a user agent are allowed. |
| `playbackRestrictionId` | string | yes | The playback restriction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `PUT /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/user_agent` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-agent-restriction.md) for the provider-specific parameters and requirements.

