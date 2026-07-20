# Notion: Update Database



```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-database', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | ID of a Notion database, a container for one or more data sources. |
| `parent` | object | no | The parent page or workspace to move the database to. |
| `title[]` | array<object> | no | The updated title of the database as a Notion rich text array. |
| `description[]` | array<object> | no | The updated description of the database as a Notion rich text array. |
| `isInline` | boolean | no | Whether the database should be displayed inline in the parent page. |
| `icon` | object | no | The updated icon for the database. |
| `cover` | object | no | The updated cover image for the database. |
| `inTrash` | boolean | no | Whether the database should be moved to or from the trash. |
| `isLocked` | boolean | no | Whether the database should be locked from editing in the Notion app UI. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Notion API returns.

## Native endpoint

Through the native Notion API, this operation is `PATCH /databases/:database_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-database.md) for the provider-specific parameters and requirements.

