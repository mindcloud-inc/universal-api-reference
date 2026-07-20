# Easy Redmine: Get Issue

Retrieves an issue from Easy Redmine.

```
GET https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-issue?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/get-issue?${params}`, {
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
| `id` | number | yes | ID of the issue to retrieve. |

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

Through the native Easy Redmine API, this operation is `GET /issues/:id.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

