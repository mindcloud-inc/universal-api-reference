# Timetonic: Create Or Update Table Row

Creates or updates a table row in Timetonic.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookOwner": "string",
  "rowId": "tmpNEW_ROW",
  "fieldValues": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-or-update-table-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookOwner": "string",
    "rowId": "tmpNEW_ROW",
    "fieldValues": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookOwner` | string | yes | Owner of the target TimeTonic book. |
| `rowId` | string | yes | Existing row id to update, or tmpNEW_ROW to create a new row. Default: `tmpNEW_ROW`. |
| `fieldValues` | string | yes | JSON object string mapping field ids to row values. |
| `viewId` | string | no | Optional view id used when creating or updating the row from a specific view. |
| `tabId` | string | no | Optional tab id used to scope the row request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkSeparator` | string | no | Optional separator for link-type values. |
| `bypassUrlTrigger` | string | no | Optional flag to disable webhooks for this mutation. |

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
| `status` | string | Provider status for the row mutation. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-table-row.md) for the provider-specific parameters and requirements.

