# Vapi: Delete Tool

Deletes an existing tool from Vapi.

```
DELETE https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-tool?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-tool?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backoffPlan": {},
      "body": {},
      "createdAt": "string",
      "credentialId": "string",
      "description": "string",
      "encryptedPaths": [
        "string"
      ],
      "headers": {},
      "id": "string",
      "messages": [
        {}
      ],
      "method": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "parameters": [
        {}
      ],
      "rejectionPlan": {},
      "timeoutSeconds": 1,
      "type": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "variableExtractionPlan": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backoffPlan` | object |  |
| `body` | object |  |
| `createdAt` | string | This is the ISO 8601 date-time string of when the tool was created. |
| `credentialId` | string | The credential ID for API request authentication |
| `description` | string | This is the description of the tool. This will be passed to the model. |
| `encryptedPaths` | array<string> | This is the paths to encrypt in the request body if credentialId and encryptionPlan are defined. |
| `headers` | object |  |
| `id` | string | This is the unique identifier for the tool. |
| `messages` | array<object> | These are the messages that will be spoken to the user as the tool is running.  For some tools, this is auto-filled based on special fields like `tool.destinations`. For others like the function tool, these can be custom configured. |
| `method` | string |  |
| `name` | string | This is the name of the tool. This will be passed to the model.  Must be a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 40. |
| `orgId` | string | This is the unique identifier for the organization that this tool belongs to. |
| `parameters` | array<object> | Static key-value pairs merged into the request body or function arguments. Values support Liquid templates. |
| `rejectionPlan` | object |  |
| `timeoutSeconds` | number | This is the timeout in seconds for the request. Defaults to 20 seconds.  @default 20 |
| `type` | string | Discriminator value: apiRequest |
| `updatedAt` | string | This is the ISO 8601 date-time string of when the tool was last updated. |
| `url` | string | This is where the request will be sent. |
| `variableExtractionPlan` | object |  |

## Native endpoint

Through the native Vapi API, this operation is `DELETE /tool/:id` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tool.md) for the provider-specific parameters and requirements.

