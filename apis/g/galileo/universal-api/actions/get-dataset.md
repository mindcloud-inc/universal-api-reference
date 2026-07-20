# Galileo: Get Dataset

Retrieves a dataset from Galileo by ID.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-dataset?${params}`, {
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
| `datasetId` | string | yes | Galileo dataset UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnNames": [
        "Ava Chen"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUser": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
      },
      "currentVersionIndex": 1,
      "draft": true,
      "id": "string",
      "name": "Ava Chen",
      "numRows": 1,
      "permissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string"
        }
      ],
      "projectCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnNames` | array<string> |  |
| `createdAt` | date |  |
| `createdByUser.email` | string |  |
| `createdByUser.firstName` | string |  |
| `createdByUser.id` | string |  |
| `createdByUser.lastName` | string |  |
| `currentVersionIndex` | number |  |
| `draft` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `numRows` | number |  |
| `permissions` | array<object> |  |
| `permissions[].action` | string |  |
| `permissions[].allowed` | boolean |  |
| `permissions[].message` | string |  |
| `projectCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/datasets/:dataset_id` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

