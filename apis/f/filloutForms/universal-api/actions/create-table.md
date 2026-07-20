# Fillout Forms: Create Table

Creates a table in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "67ef4d500c50cce9",
  "name": "Contacts",
  "fields[]": [
    {}
  ],
  "fields[].type": "attachments",
  "fields[].name": "Full Name",
  "fields[].template": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "67ef4d500c50cce9",
    "name": "Contacts",
    "fields[]": [{}],
    "fields[].type": "attachments",
    "fields[].name": "Full Name",
    "fields[].template": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The unique identifier of the database Example: `67ef4d500c50cce9`. |
| `name` | string | yes | Table name Example: `Contacts`. |
| `fields[]` | array<object> | yes | Array of field definitions to create with the table |
| `fields[].type` | list | yes | Field type One of: `attachments`, `autonumber`, `checkbox`, `currency`, `date`, `datetime`, `duration`, `email`, `linked_record`, `long_text`, `lookup`, `multiple_select`, `number`, `percent`, `phone_number`, `rating`, `single_line_text`, `single_select`, `source`, `url`. |
| `fields[].name` | string | yes | Field name Example: `Full Name`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[].template` | object | yes | Field-specific configuration options. See the Fillout field types reference for the template shape for each field type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "primaryFieldId": "string",
      "url": "https://example.com",
      "views": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Fields in the table. |
| `id` | string | Table identifier. |
| `name` | string | Table name. |
| `order` | number | Display order of the table. |
| `primaryFieldId` | string | Primary field identifier. |
| `url` | string | Table URL in Fillout. |
| `views` | array<object> | Views in the table. |

## Native endpoint

Through the native Fillout Forms API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

