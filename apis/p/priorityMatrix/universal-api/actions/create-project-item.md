# Priority Matrix: Create Project Item

Creates a new item in a Priority Matrix project.

```
POST https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "owner": "string",
  "projects[]": [
    "string"
  ],
  "quadrant": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/create-project-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "owner": "string",
    "projects[]": ["string"],
    "quadrant": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Item name. |
| `descriptionText` | string | no | Item notes in plain text. |
| `owner` | string | yes | Owner email address for the item. |
| `projects[]` | array<string> | yes | Project resource URI list, for example /api/v1/project/234/. |
| `quadrant` | number | yes | Quadrant number: 0 top-left, 1 top-right, 2 bottom-left, 3 bottom-right. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionPercentage": 1,
      "creationDate": 1,
      "descriptionText": "string",
      "id": 1,
      "name": "Ava Chen",
      "owner": "string",
      "quadrant": 1,
      "resource_uri": "string",
      "state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completionPercentage` | number |  |
| `creationDate` | number |  |
| `descriptionText` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | string |  |
| `quadrant` | number |  |
| `resource_uri` | string |  |
| `state` | number |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `POST /api/v1/item/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-item.md) for the provider-specific parameters and requirements.

