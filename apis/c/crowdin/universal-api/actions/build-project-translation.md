# Crowdin: Build Project Translation

Starts a project translation build in Crowdin.

```
POST https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/build-project-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/build-project-translation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/build-project-translation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `branchId` | number | no |  |
| `targetLanguageIds[]` | array<string> | no |  |
| `skipUntranslatedStrings` | boolean | no |  |
| `skipUntranslatedFiles` | boolean | no |  |
| `exportApprovedOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "progress": 1,
      "projectId": 1,
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | date |  |
| `finishedAt` | date |  |
| `id` | number |  |
| `progress` | number |  |
| `projectId` | number |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Crowdin API, this operation is `POST /projects/:projectId/translations/builds` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-project-translation.md) for the provider-specific parameters and requirements.

