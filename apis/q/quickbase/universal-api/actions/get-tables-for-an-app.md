# Quickbase: Get Tables for an App

Retrieves all tables in a Quickbase app.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-tables-for-an-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-tables-for-an-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-tables-for-an-app?${params}`, {
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
| `appId` | string | yes | The Quickbase app identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created": "2026-05-07T12:00:00.000Z",
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

Through the native Quickbase API, this operation is `GET v1/tables` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tables-for-an-app.md) for the provider-specific parameters and requirements.

