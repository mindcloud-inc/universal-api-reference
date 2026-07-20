# Easy Projects: Get Project

Retrieves a project from Easy Projects by ID.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Birdview project ID. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "customerId": 1,
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "projectStatusId": 1,
      "projectStatusName": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object |  |
| `customerId` | number |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `projectStatusId` | number |  |
| `projectStatusName` | string |  |
| `startDate` | date |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/projects/:id` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

