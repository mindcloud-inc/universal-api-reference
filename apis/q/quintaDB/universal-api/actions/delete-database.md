# QuintaDB: Delete Database

Deletes an existing database from QuintaDB.

```
DELETE https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-database?connectionId=$CONNECTION_ID&app_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "app_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-database?${params}`, {
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
| `app_id` | string | yes | Identifier of the QuintaDB database to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databases": [
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
| `databases` | array<object> | Remaining databases after deletion. |

## Native endpoint

Through the native QuintaDB API, this operation is `DELETE /apps/:app_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database.md) for the provider-specific parameters and requirements.

