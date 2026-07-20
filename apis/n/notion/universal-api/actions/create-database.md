# Notion: Create Database



```
POST https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | object | yes | The parent page or workspace where the database will be created. |
| `title[]` | array<object> | no | The title of the database as a Notion rich text array. |
| `description[]` | array<object> | no | The description of the database as a Notion rich text array. |
| `isInline` | boolean | no | Whether the database should be displayed inline in the parent page. |
| `initialDataSource` | object | no | Initial data source configuration for the database, including its properties schema. |
| `icon` | object | no | The icon for the database. |
| `cover` | object | no | The cover image for the database. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Notion API returns.

## Native endpoint

Through the native Notion API, this operation is `POST /databases` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.

