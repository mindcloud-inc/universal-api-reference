# MOBIDI: Create Token

Creates an access token in MOBIDI.

```
POST https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenTarget": "Any"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenTarget": "Any"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tokenTarget` | string | yes | Target scope for the generated token. Default: `Any`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `GET /MobidiTokenHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token.md) for the provider-specific parameters and requirements.

