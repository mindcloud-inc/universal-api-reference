# PixieBrix: List Database Assets

Retrieves assets from a PixieBrix database.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-database-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-database-assets?connectionId=$CONNECTION_ID&limit=25&offset=0&databasePk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "databasePk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-database-assets?${params}`, {
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
| `databasePk` | string | yes | PixieBrix database identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "download_url": "https://example.com",
      "filename": "Ava Chen",
      "id": "string",
      "is_uploaded": true,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `download_url` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `is_uploaded` | boolean |  |
| `updated_at` | date |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/databases/:database_pk/assets/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-database-assets.md) for the provider-specific parameters and requirements.

