# GoodDay.work: Create Project

Creates a new project in GoodDay.work.

```
POST https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "createdByUserId": "string",
  "projectTemplateId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "createdByUserId": "string",
    "projectTemplateId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdByUserId` | string | yes | ID of user on whose behalf project is created. |
| `projectTemplateId` | string | yes | Project template ID. |
| `name` | string | yes | Project name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "id": "string",
      "momentCreated": "string",
      "name": "Ava Chen",
      "parentProjectId": "string",
      "priority": 1,
      "startDate": "string",
      "status": "string",
      "systemStatus": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string | Project end date. |
| `id` | string | Created project ID. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Project name. |
| `parentProjectId` | string | Parent folder/project ID, if any. |
| `priority` | number | Project priority. |
| `startDate` | string | Project start date. |
| `status` | string | Project status label. |
| `systemStatus` | number | Project system status. |

## Native endpoint

Through the native GoodDay.work API, this operation is `POST /projects/new-project` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

