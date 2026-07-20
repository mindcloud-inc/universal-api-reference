# Mux: Update Referrer Playback Restriction



```
PUT https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-referrer-playback-restriction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-referrer-playback-restriction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowedDomains[]": [
    "string"
  ],
  "playbackRestrictionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-referrer-playback-restriction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowedDomains[]": ["string"],
    "playbackRestrictionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedDomains[]` | array<string> | yes | The allowed referrer domains. |
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

Through the native Mux API, this operation is `PUT /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/referrer` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-referrer-playback-restriction.md) for the provider-specific parameters and requirements.

