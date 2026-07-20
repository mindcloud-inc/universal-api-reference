# CodeREADr: Create User

Creates a new app user in CodeREADr.

```
POST https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "new.user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "new.user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | CodeREADr username for the new user. Example: `new.user@example.com`. |
| `password` | string | no | Required when username is not an email address. Example: `TempPass123!`. |
| `limit` | string | no | Optional device activation limit for the user. Example: `5`. |

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
        "id": {
          "_text": "string"
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
| `xml.id._text` | string |  |
| `xml.status._text` | string |  |

## Native endpoint

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

