# CodeREADr: List Users

Retrieves authorized app users from CodeREADr.

```
GET https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/list-users?${params}`, {
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
| `userId` | string | no | Optional user IDs to filter the list. Example: `581405`. |

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
        },
        "user": [
          {
            "_attributes": {
              "id": "string"
            },
            "created": {
              "_text": "string"
            },
            "username": {
              "_text": "Ava Chen"
            }
          }
        ]
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
| `xml.user[]._attributes.id` | string |  |
| `xml.user[].created._text` | string |  |
| `xml.user[].username._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

