# Insightful: Update Project

Updates an existing project in your Insightful account.

```
PUT https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | no | Whether the project is archived. |
| `description` | string | no | The updated project description. |
| `employees[]` | array<string> | no | Employee IDs assigned to the project. |
| `id` | string | yes | The project ID to update. |
| `name` | string | no | The updated project name. |
| `screenshotSettings` | object | no | Screenshot settings for the project. |

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

Through the native Insightful API, this operation is `PUT /project/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

