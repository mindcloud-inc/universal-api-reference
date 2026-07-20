# Outlign: List Phases By Project

Retrieves project phase records from Outlign by project.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-phases-by-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-phases-by-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-phases-by-project?${params}`, {
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
| `projectId` | number | yes | Filter phases by project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "id": 1,
        "title": "string"
      },
      "company": {
        "id": 1,
        "title": "string"
      },
      "createdAt": "string",
      "dueDate": "string",
      "id": 1,
      "isInternal": true,
      "order": 1,
      "project": {
        "id": 1,
        "title": "string"
      },
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.id` | number |  |
| `client.title` | string |  |
| `company.id` | number |  |
| `company.title` | string |  |
| `createdAt` | string |  |
| `dueDate` | string |  |
| `id` | number |  |
| `isInternal` | boolean |  |
| `order` | number |  |
| `project.id` | number |  |
| `project.title` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /phases` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phases-by-project.md) for the provider-specific parameters and requirements.

