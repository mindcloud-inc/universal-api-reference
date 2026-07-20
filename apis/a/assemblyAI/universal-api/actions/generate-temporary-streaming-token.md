# AssemblyAI: Generate Temporary Streaming Token

Retrieves a temporary streaming token from AssemblyAI.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/generate-temporary-streaming-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/generate-temporary-streaming-token?connectionId=$CONNECTION_ID&expiresInSeconds=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expiresInSeconds": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/generate-temporary-streaming-token?${params}`, {
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
| `expiresInSeconds` | number | yes | Desired token expiration in seconds. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxSessionDurationSeconds` | number | no | Maximum session duration in seconds for the generated token. Default: `10800`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresInSeconds": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresInSeconds` | number |  |
| `token` | string |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET https://streaming.assemblyai.com/v3/token` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-temporary-streaming-token.md) for the provider-specific parameters and requirements.

