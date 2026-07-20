# KiteSuite: List Project Lists

Retrieves a list from KiteSuite by list ID.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-project-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-project-lists?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-project-lists?${params}`, {
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
| `id` | string | yes | This endpoint returned a single list when called with a list ID at runtime, despite the Swagger summary implying a project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "listName": "Ava Chen",
      "projectID": {},
      "status": "string",
      "tasks": [
        {}
      ]
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
| `projectID` | object |  |
| `status` | string |  |
| `tasks` | array<object> |  |

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/list/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-lists.md) for the provider-specific parameters and requirements.

