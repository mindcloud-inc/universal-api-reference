# PixieBrix: Get Database Asset

Retrieves a database asset from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-asset?connectionId=$CONNECTION_ID&databasePk=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databasePk": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-asset?${params}`, {
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
| `id` | string | yes | PixieBrix database asset identifier. |

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

Through the native PixieBrix API, this operation is `GET /api/databases/:database_pk/assets/:id/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-asset.md) for the provider-specific parameters and requirements.

