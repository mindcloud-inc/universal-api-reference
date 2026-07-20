# CodeREADr: Retrieve Limits

Retrieves API usage limits from CodeREADr.

```
GET https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits?${params}`, {
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
        "day": {
          "_attributes": {
            "left": "string",
            "limit": "string"
          }
        },
        "minute": {
          "_attributes": {
            "left": "string",
            "limit": "string"
          }
        },
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
| `xml.day._attributes.left` | string |  |
| `xml.day._attributes.limit` | string |  |
| `xml.minute._attributes.left` | string |  |
| `xml.minute._attributes.limit` | string |  |
| `xml.status._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-limits.md) for the provider-specific parameters and requirements.

