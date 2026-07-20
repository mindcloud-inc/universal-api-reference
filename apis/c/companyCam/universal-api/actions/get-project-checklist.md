# CompanyCam: Get Project Checklist

Retrieves a project checklist from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project-checklist?connectionId=$CONNECTION_ID&projectId=string&checklistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "checklistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project-checklist?${params}`, {
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
| `projectId` | string | yes |  |
| `checklistId` | string | yes | The `id` of the Checklist you want to retrieve from the above Project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklistTemplateId": {},
      "companyId": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "id": "string",
      "isPopulating": {},
      "name": "Ava Chen",
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklistTemplateId` | object |  |
| `companyId` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `id` | string |  |
| `isPopulating` | object |  |
| `name` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET projects/:projectId/checklists/:checklistId` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-checklist.md) for the provider-specific parameters and requirements.

