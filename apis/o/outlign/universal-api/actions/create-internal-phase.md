# Outlign: Create Internal Phase

Creates a new internal phase in Outlign.

```
POST https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-internal-phase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-internal-phase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-internal-phase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The phase name. |
| `projectId` | number | yes | The project that owns the phase. |

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
| `data.createdAt` | string |  |
| `data.dueDate` | string |  |
| `data.id` | number |  |
| `data.isInternal` | boolean |  |
| `data.order` | number |  |
| `data.project.id` | number |  |
| `data.project.title` | string |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `POST /phases` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-internal-phase.md) for the provider-specific parameters and requirements.

