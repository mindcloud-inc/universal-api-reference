# CodeREADr: Upsert Database Value

Adds or updates a database value in CodeREADr.

```
PUT https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/upsert-database-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/upsert-database-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "1347442",
  "value": "ABC123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/upsert-database-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "1347442",
    "value": "ABC123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database to update. Example: `1347442`. |
| `value` | string | yes | Barcode value to insert or update. Example: `ABC123`. |
| `response` | string | no | Associated response text for the barcode. Example: `Checked in`. |
| `validity` | string | no | Set to 1 for valid or 0 for invalid. Example: `1`. |
| `trimValue` | string | no | Trim surrounding whitespace before saving. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_declaration": {
        "_attributes": {
          "encoding": "string",
          "version": "string"
        }
      },
      "xml": {
        "status": {
          "_text": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_declaration._attributes.encoding` | string |  |
| `_declaration._attributes.version` | string |  |
| `xml.status._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-database-value.md) for the provider-specific parameters and requirements.

