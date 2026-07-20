# Hume AI: Create Tool

Creates a new EVI tool in Hume AI.

```
POST https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "parameters": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "parameters": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Tool name. |
| `parameters` | string | yes | Stringified JSON schema for the tool parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "description": "string",
      "fallbackContent": "string",
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "parameters": "string",
      "toolType": "string",
      "version": 1,
      "versionDescription": "string",
      "versionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number | Creation timestamp in milliseconds. |
| `description` | string | Tool description. |
| `fallbackContent` | string | Fallback content when the tool cannot run. |
| `id` | string | Tool ID. |
| `modifiedOn` | number | Last modification timestamp in milliseconds. |
| `name` | string | Tool name. |
| `parameters` | string | JSON Schema parameters as a serialized string. |
| `toolType` | string | Tool type. |
| `version` | number | Tool version number. |
| `versionDescription` | string | Optional version description. |
| `versionType` | string | Tool version type. |

## Native endpoint

Through the native Hume AI API, this operation is `POST /v0/evi/tools` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tool.md) for the provider-specific parameters and requirements.

