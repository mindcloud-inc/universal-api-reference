# Airtable: Create Table

Creates a new table in a specific Airtable base.

```
POST https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "name": "Ava Chen",
  "fields[]": [
    {}
  ],
  "fields[].name": "Ava Chen",
  "fields[].type": "aiText"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "name": "Ava Chen",
    "fields[]": [{}],
    "fields[].name": "Ava Chen",
    "fields[].type": "aiText"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | list<string> | yes |  |
| `name` | string | yes |  |
| `fields[]` | array<object> | yes |  |
| `fields[].name` | string | yes |  |
| `fields[].type` | list<string> | yes | One of: `aiText`, `autoNumber`, `barcode`, `button`, `checkbox`, `count`, `createdBy`, `createdTime`, `currency`, `date`, `dateTime`, `duration`, `email`, `externalSyncSource`, `formula`, `lastModifiedBy`, `lastModifiedTime`, `lookup`, `multilineText`, `multipleAttachments`, `multipleCollaborators`, `multipleRecordLinks`, `multipleSelects`, `number`, `percent`, `phoneNumber`, `rating`, `richText`, `rollup`, `singleCollaborator`, `singleLineText`, `singleSelect`, `url`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `fields[].description` | string | no |  |
| `fields[].options` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "primaryFieldId": "string",
      "views": [
        {
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].id` | string |  |
| `fields[].name` | string |  |
| `fields[].type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `primaryFieldId` | string |  |
| `views[].id` | string |  |
| `views[].name` | string |  |
| `views[].type` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `POST /meta/bases/:baseId/tables` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

