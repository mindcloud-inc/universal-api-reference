# Smartcat: List Projects

Retrieves projects from the current Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "assignmentMode": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "description": "string",
      "documents": [
        {}
      ],
      "externalTag": "string",
      "id": "string",
      "managers": [
        {}
      ],
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "sourceLanguage": "string",
      "sourceLanguageId": 1,
      "specializations": [
        {}
      ],
      "status": "string",
      "statusModificationDate": "2026-05-07T12:00:00.000Z",
      "targetLanguages": [
        "string"
      ],
      "vendors": [
        {}
      ],
      "workflowStages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `assignmentMode` | string |  |
| `creationDate` | date |  |
| `customFields` | object |  |
| `description` | string |  |
| `documents` | array<object> |  |
| `externalTag` | string |  |
| `id` | string |  |
| `managers` | array<object> |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `sourceLanguage` | string |  |
| `sourceLanguageId` | number |  |
| `specializations` | array<object> |  |
| `status` | string |  |
| `statusModificationDate` | date |  |
| `targetLanguages` | array<string> |  |
| `vendors` | array<object> |  |
| `workflowStages` | array<object> |  |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/project/list` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

