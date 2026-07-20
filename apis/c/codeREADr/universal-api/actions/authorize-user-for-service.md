# CodeREADr: Authorize User for Service

Authorizes an app user for a scanning service in CodeREADr.

```
PUT https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/authorize-user-for-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeREADr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/authorize-user-for-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceId": "2231648",
  "userId": "581405"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/authorize-user-for-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceId": "2231648",
    "userId": "581405"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceId` | string | yes | Service or services to authorize the user for. Example: `2231648`. |
| `userId` | string | yes | User or users to authorize for the service. Example: `581405`. |

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

Through the native CodeREADr API, this operation is `POST /api/` (base URL `https://api.codereadr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize-user-for-service.md) for the provider-specific parameters and requirements.

