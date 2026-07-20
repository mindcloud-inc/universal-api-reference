# Deepgram: Create Project Key

Creates a new project API key in Deepgram.

```
POST https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/create-project-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/create-project-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "scopes": "string",
  "expirationDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/create-project-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "scopes": "string",
    "expirationDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Deepgram project identifier. |
| `scopes` | string | yes | Scopes to grant to the created project key. |
| `expirationDate` | string | yes | Expiration timestamp for the created project key in ISO 8601 format. |
| `comment` | string | no | Human-readable comment stored with the project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "comment": "string",
      "created": "string",
      "expirationDate": "string",
      "key": "string",
      "scopes": [
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
| `apiKeyId` | string |  |
| `comment` | string |  |
| `created` | string |  |
| `expirationDate` | string |  |
| `key` | string |  |
| `scopes` | array<string> |  |

## Native endpoint

Through the native Deepgram API, this operation is `POST /v1/projects/:project_id/keys` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-key.md) for the provider-specific parameters and requirements.

