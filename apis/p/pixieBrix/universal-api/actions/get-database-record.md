# PixieBrix: Get Database Record

Retrieves a record from a PixieBrix database.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-record?connectionId=$CONNECTION_ID&databasePk=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databasePk": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-database-record?${params}`, {
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
| `key` | string | yes | PixieBrix database record key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `data` | object |  |
| `id` | string |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/databases/:database_pk/records/:key/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-record.md) for the provider-specific parameters and requirements.

