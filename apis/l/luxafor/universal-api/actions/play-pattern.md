# Luxafor: Play Pattern

Updates a Luxafor device by playing a pattern.

```
PUT https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/play-pattern
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Luxafor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/play-pattern" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionFields.pattern": "police"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/play-pattern', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionFields.pattern": "police"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionFields` | object | no |  |
| `actionFields.pattern` | string | yes | Accepted patterns: police, traffic lights, random 1, random 2, random 3, random 4, random 5. Windows-only patterns: rainbow, sea, white wave, synthetic. Example: `police`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Luxafor API returns.

## Native endpoint

Through the native Luxafor API, this operation is `POST /pattern` (base URL `https://api.luxafor.com/webhook/v1/actions`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/play-pattern.md) for the provider-specific parameters and requirements.

