# Zite: Get Database by ID

Retrieves a specific database from Zite by ID.

```
GET https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-database-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-database-by-id?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-database-by-id?${params}`, {
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
| `databaseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `tables` | array<object> |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Zite API, this operation is `GET /bases/:databaseId` (base URL `https://tables.fillout.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-by-id.md) for the provider-specific parameters and requirements.

