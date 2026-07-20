# HeadshotPro: Create Model

Creates a new model in HeadshotPro.

```
POST https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the user who should receive the HeadshotPro session. |
| `teamId` | string | no | Optional team assignment for the new model. |
| `version` | string | no | Optional model generation version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "modelId": "string",
      "signedUrl": "https://example.com",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modelId` | string | Created model ID. |
| `signedUrl` | string | Signed whitelabel onboarding URL. |
| `status` | string | Initial model status. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `POST /organization/models` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

