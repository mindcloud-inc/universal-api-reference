# Cerebras AI: Update Model Version Aliases

Updates model version aliases in Cerebras AI.

```
PUT https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/update-model-version-aliases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/update-model-version-aliases" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgName": "Ava Chen",
  "modelArchId": "string",
  "versionId": "string",
  "versionAliases[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/update-model-version-aliases', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgName": "Ava Chen",
    "modelArchId": "string",
    "versionId": "string",
    "versionAliases[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgName` | string | yes |  |
| `modelArchId` | string | yes |  |
| `versionId` | string | yes |  |
| `versionAliases[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "versionAliases": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `versionAliases` | array<string> |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `PATCH /management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model-version-aliases.md) for the provider-specific parameters and requirements.

