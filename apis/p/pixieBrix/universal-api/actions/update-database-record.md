# PixieBrix: Update Database Record

Updates a database record in PixieBrix, creating it if needed.

```
PUT https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/update-database-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/update-database-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "databasePk": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/update-database-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "databasePk": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Updated record data object. |
| `databasePk` | string | yes | PixieBrix database identifier. |
| `id` | string | yes | Record id/key to update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergeStrategy` | string | no | How PixieBrix should merge record data. Defaults to replace. One of: `0`, `1`, `2`, `3`. Default: `replace`. |

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

Through the native PixieBrix API, this operation is `PUT /api/databases/:database_pk/records/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-database-record.md) for the provider-specific parameters and requirements.

