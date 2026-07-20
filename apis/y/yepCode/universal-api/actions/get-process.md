# YepCode: Get process

Retrieves details for a process from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process?${params}`, {
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
| `identifier` | string | yes | Unique identifier of the process to retrieve. You can use either the process UUID or slug. |

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
        "description": "string",
        "title": "string",
        "type": "string"
      },
      "programmingLanguage": "string",
      "readme": "string",
      "settings": {
        "dependencies": {
          "autoDetect": true,
          "scopedToProcess": true
        },
        "formsConfig": {
          "enabled": true
        },
        "publicConfig": {
          "enabled": true
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
| `parametersSchema.description` | string |  |
| `parametersSchema.title` | string |  |
| `parametersSchema.type` | string |  |
| `programmingLanguage` | string |  |
| `readme` | string |  |
| `settings.dependencies.autoDetect` | boolean |  |
| `settings.dependencies.scopedToProcess` | boolean |  |
| `settings.formsConfig.enabled` | boolean |  |
| `settings.publicConfig.enabled` | boolean |  |
| `slug` | string |  |
| `sourceCode` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `webhook.enabled` | boolean |  |

## Native endpoint

Through the native YepCode API, this operation is `GET /processes/:identifier` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process.md) for the provider-specific parameters and requirements.

