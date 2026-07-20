# Digital Humani: Plant Trees

Creates a tree-planting request in Digital Humani.

```
POST https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/plant-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/plant-trees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "treeCount": 1,
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/plant-trees', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "treeCount": 1,
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The Digital Humani project ID where the trees should be planted. |
| `treeCount` | number | yes | The number of trees to plant. |
| `user` | string | yes | The end user associated with the tree-planting request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "enterpriseId": "string",
      "projectId": "string",
      "treeCount": 1,
      "user": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `enterpriseId` | string |  |
| `projectId` | string |  |
| `treeCount` | number |  |
| `user` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Digital Humani API, this operation is `POST /tree` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/plant-trees.md) for the provider-specific parameters and requirements.

