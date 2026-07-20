# Outlign: Get Task

Retrieves a specific task from Outlign.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-task?${params}`, {
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
| `id` | number | yes | Task ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "client": {
          "id": 1,
          "title": "string"
        },
        "company": {
          "id": 1,
          "title": "string"
        },
        "completed": true,
        "createdAt": "string",
        "dueDate": "string",
        "id": 1,
        "phase": {
          "id": 1,
          "isInternal": true,
          "title": "string"
        },
        "project": {
          "id": 1,
          "title": "string"
        },
        "published": true,
        "title": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.client.id` | number |  |
| `data.client.title` | string |  |
| `data.company.id` | number |  |
| `data.company.title` | string |  |
| `data.completed` | boolean |  |
| `data.createdAt` | string |  |
| `data.dueDate` | string |  |
| `data.id` | number |  |
| `data.phase.id` | number |  |
| `data.phase.isInternal` | boolean |  |
| `data.phase.title` | string |  |
| `data.project.id` | number |  |
| `data.project.title` | string |  |
| `data.published` | boolean |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /steps/:id` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

