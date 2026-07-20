# Outlign: Get Project

Retrieves a specific project from Outlign.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | ID of the project to retrieve |

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
        "clientProjectType": "string",
        "company": {
          "id": 1,
          "title": "string"
        },
        "createdAt": "string",
        "description": "string",
        "id": 1,
        "internalProjectType": "string",
        "isClient": true,
        "isInternal": true,
        "members": [
          {
            "id": 1,
            "name": "Ava Chen"
          }
        ],
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
| `data.clientProjectType` | string |  |
| `data.company.id` | number |  |
| `data.company.title` | string |  |
| `data.createdAt` | string |  |
| `data.description` | string |  |
| `data.id` | number |  |
| `data.internalProjectType` | string |  |
| `data.isClient` | boolean |  |
| `data.isInternal` | boolean |  |
| `data.members[].id` | number |  |
| `data.members[].name` | string |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /projects/:id` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

