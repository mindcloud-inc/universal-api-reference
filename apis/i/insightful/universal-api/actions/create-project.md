# Insightful: Create Project

Creates a new project in your Insightful account.

```
POST https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employees[]": [
    "string"
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employees[]": ["string"],
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | boolean | no | Whether the project is billable. |
| `deadline` | number | no | Project deadline in milliseconds. |
| `description` | string | no | A description for the project. |
| `employees[]` | array<string> | yes | Employee IDs to assign to the project. |
| `name` | string | yes | The project name. |
| `payroll` | object | no | Payroll settings for the project. |
| `priorities[]` | array<string> | no | Possible project priorities. |
| `statuses[]` | array<string> | no | Possible project statuses. |

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

Through the native Insightful API, this operation is `POST /project` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

