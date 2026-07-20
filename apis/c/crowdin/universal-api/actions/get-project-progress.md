# Crowdin: Get Project Progress

Retrieves project progress by language from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-project-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-project-progress?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-project-progress?${params}`, {
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
| `projectId` | number | yes |  |
| `languageIds[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalProgress": 1,
      "language": {},
      "languageId": "string",
      "phrases": {},
      "qaChecksStatus": {},
      "translationProgress": 1,
      "words": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalProgress` | number |  |
| `language` | object |  |
| `languageId` | string |  |
| `phrases` | object |  |
| `qaChecksStatus` | object |  |
| `translationProgress` | number |  |
| `words` | object |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/languages/progress` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-project-progress.md) for the provider-specific parameters and requirements.

