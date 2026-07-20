# E2B: Connect To Sandbox

Retrieves sandbox details from E2B and resumes it if paused.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/connect-to-sandbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/connect-to-sandbox?connectionId=$CONNECTION_ID&sandboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/connect-to-sandbox?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxId` | string | yes | Identifier of the sandbox. |

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

Through the native E2B API, this operation is `POST /sandboxes/{sandboxID}/connect` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-to-sandbox.md) for the provider-specific parameters and requirements.

