# Crowdin: List Projects

Retrieves projects from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-projects?${params}`, {
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
| `orderBy` | string | no |  |
| `userId` | number | no |  |
| `hasManagerAccess` | boolean | no |  |
| `type` | number | no |  |

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

Through the native Crowdin API, this operation is `GET /projects` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

