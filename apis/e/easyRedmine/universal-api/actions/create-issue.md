# Easy Redmine: Create Issue

Creates a new issue in Easy Redmine.

```
POST https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issue": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issue": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issue` | object | yes | Issue payload to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "priority": {},
      "project": {},
      "status": {},
      "subject": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object |  |
| `createdOn` | date |  |
| `description` | string |  |
| `id` | number |  |
| `priority` | object |  |
| `project` | object |  |
| `status` | object |  |
| `subject` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `POST /issues.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

