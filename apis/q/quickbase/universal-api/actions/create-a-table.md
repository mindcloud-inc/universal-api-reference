# Quickbase: Create a Table

Creates a new table in Quickbase.

```
POST https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The Quickbase app identifier. |
| `name` | string | yes | The table name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the table. |
| `singleRecordName` | string | no | Optional singular label for records in the table. |
| `pluralRecordName` | string | no | Optional plural label for records in the table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "defaultSortFieldId": 1,
      "defaultSortOrder": "string",
      "description": "string",
      "id": "string",
      "keyFieldId": 1,
      "name": "Ava Chen",
      "nextFieldId": 1,
      "nextRecordId": 1,
      "pluralRecordName": "Ava Chen",
      "singleRecordName": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | The table alias. |
| `created` | date | When the table was created. |
| `defaultSortFieldId` | number | The default sort field ID. |
| `defaultSortOrder` | string | The default sort order. |
| `description` | string | The table description. |
| `id` | string | The Quickbase table identifier. |
| `keyFieldId` | number | The field ID used as the table key. |
| `name` | string | The table name. |
| `nextFieldId` | number | The next field ID. |
| `nextRecordId` | number | The next record ID. |
| `pluralRecordName` | string | The plural record label. |
| `singleRecordName` | string | The singular record label. |
| `updated` | date | When the table was last updated. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/tables` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-table.md) for the provider-specific parameters and requirements.

