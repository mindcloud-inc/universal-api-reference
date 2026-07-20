# Crowdin: Add Project

Creates a new project in Crowdin.

```
POST https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sourceLanguageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sourceLanguageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `sourceLanguageId` | string | yes |  |
| `targetLanguageIds[]` | array<string> | no |  |
| `visibility` | string | no |  |
| `languageAccessPolicy` | string | no | Defines access to project languages. Use `open` when the current Crowdin plan does not support moderated language membership. Default: `open`. |
| `description` | string | no |  |
| `identifier` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cname": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "identifier": "string",
      "languageAccessPolicy": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "logo": "string",
      "name": "Ava Chen",
      "publicDownloads": true,
      "saveMetaInfoInSource": true,
      "skipUntranslatedFiles": true,
      "sourceLanguage": {},
      "sourceLanguageId": "string",
      "targetLanguageIds": [
        "string"
      ],
      "targetLanguages": [
        {}
      ],
      "tmContextType": "string",
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "visibility": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cname` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `languageAccessPolicy` | string |  |
| `lastActivity` | date |  |
| `logo` | string |  |
| `name` | string |  |
| `publicDownloads` | boolean |  |
| `saveMetaInfoInSource` | boolean |  |
| `skipUntranslatedFiles` | boolean |  |
| `sourceLanguage` | object |  |
| `sourceLanguageId` | string |  |
| `targetLanguageIds` | array<string> |  |
| `targetLanguages` | array<object> |  |
| `tmContextType` | string |  |
| `type` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `visibility` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Crowdin API, this operation is `POST /projects` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project.md) for the provider-specific parameters and requirements.

