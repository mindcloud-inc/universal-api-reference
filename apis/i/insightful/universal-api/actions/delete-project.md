# Insightful: Delete Project

Deletes a project from your Insightful account.

```
DELETE https://connect.mindcloud.co/v1/universal/insightful/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/delete-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/delete-project?${params}`, {
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
| `id` | string | yes | The project ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "description": "string",
      "employees": [
        "string"
      ],
      "id": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "payroll": {
        "billRate": 1,
        "overtimeBillRate": 1
      },
      "priorities": [
        "string"
      ],
      "screenshotSettings": {
        "screenshotEnabled": true
      },
      "statuses": [
        "string"
      ],
      "teams": [
        "string"
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billable` | boolean |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `description` | string |  |
| `employees[]` | string |  |
| `id` | string |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `payroll.billRate` | number |  |
| `payroll.overtimeBillRate` | number |  |
| `priorities[]` | string |  |
| `screenshotSettings.screenshotEnabled` | boolean |  |
| `statuses[]` | string |  |
| `teams[]` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `DELETE /project/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

