# E2B: Create Sandbox

Creates a sandbox from a template in E2B.

```
POST https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Identifier of the required template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "clientID": "string",
      "domain": "https://example.com",
      "envdAccessToken": "string",
      "envdVersion": "string",
      "sandboxID": "string",
      "templateID": "string",
      "trafficAccessToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Template alias. |
| `clientID` | string | Deprecated client identifier. |
| `domain` | string | Sandbox domain. |
| `envdAccessToken` | string | Access token for envd. |
| `envdVersion` | string | Version of envd running in the sandbox. |
| `sandboxID` | string | Identifier of the sandbox. |
| `templateID` | string | Identifier of the template used for the sandbox. |
| `trafficAccessToken` | string | Access token for sandbox traffic. |

## Native endpoint

Through the native E2B API, this operation is `POST /sandboxes` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sandbox.md) for the provider-specific parameters and requirements.

