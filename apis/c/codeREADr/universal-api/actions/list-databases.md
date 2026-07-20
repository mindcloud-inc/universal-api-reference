# CodeREADr: List Databases

Retrieves validation databases from your CodeREADr account.

```
GET https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-databases?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
        "database": {
          "_attributes": {
            "id": "string"
          },
          "case_sensitivity": {
            "_text": "string"
          },
          "count": {
            "_text": "string"
          },
          "name": {
            "_text": "Ava Chen"
          },
          "solutions": {
            "_attributes": {
              "count": "string"
            }
          },
          "timestamp": {
            "_text": "string"
          }
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
| `xml.database._attributes.id` | string |  |
| `xml.database.case_sensitivity._text` | string |  |
| `xml.database.count._text` | string |  |
| `xml.database.name._text` | string |  |
| `xml.database.solutions._attributes.count` | string |  |
| `xml.database.timestamp._text` | string |  |
| `xml.status._text` | string |  |
| `xml.totalCount._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

