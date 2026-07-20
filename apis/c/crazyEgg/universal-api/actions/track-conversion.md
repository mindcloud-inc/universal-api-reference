# Crazy Egg: Track Conversion



```
POST https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/track-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crazy Egg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/track-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "goalConversions[].goalName": "Ava Chen",
  "goalConversions[].userIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/track-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "goalConversions[].goalName": "Ava Chen",
    "goalConversions[].userIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goalConversions[].goalName` | string | yes |  |
| `goalConversions[].userIdentifier` | string | yes |  |
| `goalConversions[].url` | string | no |  |
| `goalConversions[].value` | number | no |  |
| `goalConversions[].currency` | string | no |  |
| `goalConversions[].visitCount` | number | no |  |
| `goalConversions[].landingPage` | string | no |  |
| `goalConversions[].referrer` | string | no |  |
| `goalConversions[].country` | string | no |  |
| `goalConversions[].userAgent` | string | no |  |
| `goalConversions[].timestamp` | string | no |  |
| `goalConversions[].utmParams.source` | string | no |  |
| `goalConversions[].utmParams.medium` | string | no |  |
| `goalConversions[].utmParams.term` | string | no |  |
| `goalConversions[].utmParams.content` | string | no |  |
| `goalConversions[].utmParams.campaign` | string | no |  |
| `goalConversions[].customData` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Crazy Egg API, this operation is `POST https://track.crazyegg.com/api/v1` (base URL `https://app.crazyegg.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-conversion.md) for the provider-specific parameters and requirements.

