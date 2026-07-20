# Vooplayer: Add Whitelisted Domain

Creates a whitelisted domain in Vooplayer.

```
POST https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/add-whitelisted-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/add-whitelisted-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/add-whitelisted-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Desired domain, for example example.com. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vooplayer API returns.

## Native endpoint

Through the native Vooplayer API, this operation is `POST /api/user/domain` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-whitelisted-domain.md) for the provider-specific parameters and requirements.

