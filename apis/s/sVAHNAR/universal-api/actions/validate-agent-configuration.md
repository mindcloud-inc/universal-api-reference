# SVAHNAR: Validate Agent Configuration

Validates an agent configuration in SVAHNAR.

```
GET https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/validate-agent-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/validate-agent-configuration?connectionId=$CONNECTION_ID&yamlString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "yamlString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/validate-agent-configuration?${params}`, {
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
| `yamlString` | string | yes | YAML string to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "request_metadata": {},
      "status": "string",
      "suggestion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Detailed validation outcome message. |
| `request_metadata` | object | Response metadata including the request ID. |
| `status` | string | Validation result status. |
| `suggestion` | string | Optional suggestion when validation finds issues. |

## Native endpoint

Through the native SVAHNAR API, this operation is `POST /v1/agents/validate` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-agent-configuration.md) for the provider-specific parameters and requirements.

