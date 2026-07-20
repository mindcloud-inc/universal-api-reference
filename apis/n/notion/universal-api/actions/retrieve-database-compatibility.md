# Notion: Retrieve Database (Compatibility)

Retrieves a database from Notion's compatibility endpoint.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-database-compatibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-database-compatibility?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-database-compatibility?${params}`, {
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
| `databaseId` | string | yes | ID of the database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "title": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Database identifier. |
| `lastEditedTime` | date | Last edit timestamp. |
| `object` | string | Returned object type. |
| `title` | array<object> | Database title rich text array. |
| `url` | string | Database URL. |

## Native endpoint

Through the native Notion API, this operation is `GET /databases/:database_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-database-compatibility.md) for the provider-specific parameters and requirements.

