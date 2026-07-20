# KiteSuite: Update List

Updates an existing list in KiteSuite.

```
PUT https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "listName": "Ava Chen",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "listName": "Ava Chen",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | List ID. |
| `listName` | string | yes | Updated list name. |
| `status` | string | yes | Updated list status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "listName": "Ava Chen",
      "projectID": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `listName` | string |  |
| `projectID` | string |  |
| `status` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `PATCH /api/v1/list/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

