# CodeREADr: Delete Database Value

Deletes a database value from CodeREADr.

```
DELETE https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/delete-database-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/delete-database-value?connectionId=$CONNECTION_ID&databaseId=1347442&value=ABC123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "1347442",
  "value": "ABC123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/delete-database-value?${params}`, {
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
| `databaseId` | string | yes | Database to delete the value from. Example: `1347442`. |
| `value` | string | yes | Barcode value to delete. Example: `ABC123`. |

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

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database-value.md) for the provider-specific parameters and requirements.

