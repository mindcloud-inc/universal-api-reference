# CodeREADr: List Database Values

Retrieves values from a validation database in CodeREADr.

```
GET https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-database-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-database-values?connectionId=$CONNECTION_ID&databaseId=1347442" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "1347442"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-database-values?${params}`, {
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
| `databaseId` | string | yes | Database to search. Example: `1347442`. |
| `value` | string | no | Exact barcode value match. Example: `ABC123`. |
| `valueLike` | string | no | Partial barcode value match. Example: `ABC`. |
| `response` | string | no | Exact response text match. Example: `Checked in`. |
| `responseLike` | string | no | Partial response text match. Example: `Checked`. |
| `validity` | string | no | Filter by valid (1) or invalid (0). Example: `1`. |
| `limit` | string | no | Maximum number of results to return. Example: `50`. |
| `offset` | string | no | Result offset when limit is provided. Example: `0`. |

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
        "count": {
          "_text": "string"
        },
        "status": {
          "_text": "string"
        },
        "totalCount": {
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
| `xml.count._text` | string |  |
| `xml.status._text` | string |  |
| `xml.totalCount._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-values.md) for the provider-specific parameters and requirements.

