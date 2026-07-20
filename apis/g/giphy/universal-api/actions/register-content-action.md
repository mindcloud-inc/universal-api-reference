# Giphy: Register Content Action

Registers a GIF or sticker interaction in Giphy analytics.

```
POST https://connect.mindcloud.co/v1/universal/giphy/latest/actions/register-content-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/register-content-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "analyticsResponsePayload": "string",
  "actionType": "string",
  "randomId": "string",
  "ts": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giphy/latest/actions/register-content-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "analyticsResponsePayload": "string",
    "actionType": "string",
    "randomId": "string",
    "ts": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `analyticsResponsePayload` | string | yes |  |
| `actionType` | string | yes |  |
| `randomId` | string | yes |  |
| `ts` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |

## Native endpoint

Through the native Giphy API, this operation is `GET https://giphy-analytics.giphy.com/v2/pingback_simple` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-content-action.md) for the provider-specific parameters and requirements.

