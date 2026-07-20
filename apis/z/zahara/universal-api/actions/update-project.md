# Zahara: Update Project

Updates an existing project in Zahara.

```
PUT https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "27166",
  "projectName": "Ava Chen",
  "projectCode": "string",
  "description": "string",
  "budgetedAmount": 1,
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "27166",
    "projectName": "Ava Chen",
    "projectCode": "string",
    "description": "string",
    "budgetedAmount": 1,
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The Zahara project ID to update. Example: `27166`. |
| `projectName` | string | yes | Project name. |
| `projectCode` | string | yes | Project code. |
| `description` | string | yes | Project description. |
| `budgetedAmount` | number | yes | Budgeted amount. |
| `start` | date | yes | Project start date. |
| `end` | date | yes | Project end date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ProjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ProjectId` | number | Project ID represented for successful update operations in MindCloud. |

## Native endpoint

Through the native Zahara API, this operation is `PUT /api/{{credentials.businessUnitApiKey}}/Project/Update/{{projectId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

