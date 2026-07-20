# QuintaDB: Create Database

Creates a new database in QuintaDB.

```
POST https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "database_name": "Ava Chen",
  "form_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "database_name": "Ava Chen",
    "form_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `database_name` | string | yes | Name for the new QuintaDB database. |
| `form_name` | string | yes | Default form name created with the new QuintaDB database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "database": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `database` | object | Created QuintaDB database. |

## Native endpoint

Through the native QuintaDB API, this operation is `POST /apps.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.

