# Sumsub: Generate Access Token



```
POST https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/generate-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/generate-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "mindcloud-codex-sandbox-20260422-01",
  "levelName": "id-only"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/generate-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "mindcloud-codex-sandbox-20260422-01",
    "levelName": "id-only"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | Applicant identifier on your side. Example: `mindcloud-codex-sandbox-20260422-01`. |
| `levelName` | string | yes | Verification level used for the SDK token. Example: `id-only`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ttlInSecs` | number | no | Token lifespan in seconds. Sumsub defaults this value to 600 when omitted. Default: `600`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumsub API returns.

## Native endpoint

Through the native Sumsub API, this operation is `POST /resources/accessTokens/sdk` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-access-token.md) for the provider-specific parameters and requirements.

