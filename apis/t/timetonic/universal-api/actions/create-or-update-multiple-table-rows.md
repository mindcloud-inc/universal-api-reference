# Timetonic: Create Or Update Multiple Table Rows

Creates or updates multiple table rows in Timetonic.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-multiple-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-multiple-table-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookOwner": "string",
  "rows": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-multiple-table-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookOwner": "string",
    "rows": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookOwner` | string | yes | Owner of the target TimeTonic book. |
| `rows` | string | yes | JSON object string keyed by row ids or temporary ids, each containing field id to value mappings. |
| `viewId` | string | no | Optional view id used when creating or updating rows from a specific view. |
| `tabId` | string | no | Optional tab id used to scope the batch row request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "formLastModified": 1,
      "newRows": [
        {}
      ],
      "readOnlyRowsStatus": [
        {}
      ],
      "req": "string",
      "rows": [
        {}
      ],
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string | TimeTonic backend version string. |
| `formLastModified` | number | Last modified stamp for the form after the mutation. |
| `newRows` | array<object> | Rows created during the request. |
| `readOnlyRowsStatus` | array<object> | Read-only status payloads for affected rows, when present. |
| `req` | string | Echoed provider request name. |
| `rows` | array<object> | Returned row payloads after the mutation. |
| `status` | string | Provider status for the batch row mutation. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-multiple-table-rows.md) for the provider-specific parameters and requirements.

