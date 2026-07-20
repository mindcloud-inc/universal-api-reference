# Fillout: Get Database By Id

Retrieves a database from Fillout by ID.

```
GET https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-database-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-database-by-id?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-database-by-id?${params}`, {
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
| `databaseId` | string | yes | The database identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ],
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tables` | array<object> |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fillout API, this operation is `GET https://tables.fillout.com/api/v1/bases/:databaseId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-by-id.md) for the provider-specific parameters and requirements.

