# Fillout Forms: Get Database by ID

Retrieves a database by ID from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-database-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-database-by-id?connectionId=$CONNECTION_ID&databaseId=bad4b276-f604-47ad-86e5-d2ae4f60968f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "bad4b276-f604-47ad-86e5-d2ae4f60968f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-database-by-id?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database Example: `bad4b276-f604-47ad-86e5-d2ae4f60968f`. |

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
| `createdAt` | string | Database creation timestamp. |
| `id` | string | Database identifier. |
| `name` | string | Database name. |
| `tables` | array<object> | Tables in the database. |
| `updatedAt` | string | Database update timestamp. |
| `url` | string | Database URL in Fillout. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET https://tables.fillout.com/api/v1/bases/:databaseId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-by-id.md) for the provider-specific parameters and requirements.

