# CodeREADr: Create Service

Creates a new scanning service in CodeREADr.

```
POST https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "validationMethod": "record"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/create-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "validationMethod": "record"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validationMethod` | string | yes | Service type to create, such as record, database, postback, or webview. Example: `record`. |
| `databaseId` | string | no | Required when validation_method is database or ondevicedatabase. Example: `1347442`. |
| `postbackUrl` | string | no | Required when validation_method is postback. Example: `https://example.com/postback`. |
| `serviceName` | string | no | Optional name for the new service. Example: `Event Check-In`. |
| `description` | string | no | Optional service description or webview HTML/URL. Example: `Optional service description`. |

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

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service.md) for the provider-specific parameters and requirements.

