# Galileo: Get Integration

Retrieves an integration from Galileo by name.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration?${params}`, {
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
| `name` | string | yes | Integration name from Galileo, for example openai or anthropic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentialType": "string",
      "extra": {},
      "id": "string",
      "inferenceProfiles": {},
      "multiModalConfig": {
        "maxFiles": 1,
        "maxFileSizeBytes": 1
      },
      "name": "Ava Chen",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentialType` | string |  |
| `extra` | object |  |
| `id` | string |  |
| `inferenceProfiles` | object |  |
| `multiModalConfig.maxFiles` | number |  |
| `multiModalConfig.maxFileSizeBytes` | number |  |
| `name` | string |  |
| `region` | string |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/integrations/:name` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration.md) for the provider-specific parameters and requirements.

