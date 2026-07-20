# YepCode: Create process

Creates a new process in YepCode.

```
POST https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slug": "string",
  "programmingLanguage": "string",
  "sourceCode": "string",
  "parametersSchema": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slug": "string",
    "programmingLanguage": "string",
    "sourceCode": "string",
    "parametersSchema": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `slug` | string | yes |  |
| `programmingLanguage` | string | yes |  |
| `sourceCode` | string | yes |  |
| `parametersSchema` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parametersSchema": {
        "type": "string"
      },
      "programmingLanguage": "string",
      "settings": {
        "dependencies": {
          "autoDetect": true,
          "scopedToProcess": true
        },
        "formsConfig": {
          "enabled": true
        },
        "publicConfig": {
          "enabled": true,
          "token": "string"
        }
      },
      "slug": "string",
      "sourceCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "webhook": {
        "enabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `parametersSchema.type` | string |  |
| `programmingLanguage` | string |  |
| `settings.dependencies.autoDetect` | boolean |  |
| `settings.dependencies.scopedToProcess` | boolean |  |
| `settings.formsConfig.enabled` | boolean |  |
| `settings.publicConfig.enabled` | boolean |  |
| `settings.publicConfig.token` | string |  |
| `slug` | string |  |
| `sourceCode` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `webhook.enabled` | boolean |  |

## Native endpoint

Through the native YepCode API, this operation is `POST /processes` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-process.md) for the provider-specific parameters and requirements.

