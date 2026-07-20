# Fillout Forms: Create Database

Creates a database in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Customer Database",
  "tables[]": [
    {}
  ],
  "tables[].name": "Contacts",
  "tables[].fields[]": [
    {}
  ],
  "tables[].fields[].type": "attachments",
  "tables[].fields[].name": "Full Name",
  "tables[].fields[].template": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Customer Database",
    "tables[]": [{}],
    "tables[].name": "Contacts",
    "tables[].fields[]": [{}],
    "tables[].fields[].type": "attachments",
    "tables[].fields[].name": "Full Name",
    "tables[].fields[].template": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Database name Example: `Customer Database`. |
| `tables[]` | array<object> | yes | Array of table definitions to create with the database |
| `tables[].name` | string | yes | Table name Example: `Contacts`. |
| `tables[].fields[]` | array<object> | yes | Array of field definitions to create with the table |
| `tables[].fields[].type` | list | yes | Field type One of: `attachments`, `autonumber`, `checkbox`, `currency`, `date`, `datetime`, `duration`, `email`, `linked_record`, `long_text`, `lookup`, `multiple_select`, `number`, `percent`, `phone_number`, `rating`, `single_line_text`, `single_select`, `source`, `url`. |
| `tables[].fields[].name` | string | yes | Field name Example: `Full Name`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tables[].fields[].template` | object | yes | Field-specific configuration options. See the Fillout field types reference for the template shape for each field type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ],
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Database creation timestamp. |
| `id` | string | Database identifier. |
| `name` | string | Database name. |
| `tables` | array<object> | Tables in the database. |
| `updatedAt` | string | Database update timestamp. |
| `url` | string | Database URL in Fillout. |

## Native endpoint

Through the native Fillout Forms API, this operation is `POST https://tables.fillout.com/api/v1/bases` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.

