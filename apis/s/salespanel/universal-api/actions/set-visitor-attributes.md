# Salespanel: Set Visitor Attributes

Updates custom visitor attributes in Salespanel.

```
PUT https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/set-visitor-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/set-visitor-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "visitorIdentifier": "string",
  "visitorAttributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/set-visitor-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "visitorIdentifier": "string",
    "visitorAttributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visitorIdentifier` | string | yes | Contact ID or email of the visitor. |
| `visitorAttributes` | object | yes | Key-value pairs to set for the visitor. |
| `createNew` | boolean | no | Create a new visitor if the email does not already exist. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Salespanel API, this operation is `POST /visitor-attributes/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-visitor-attributes.md) for the provider-specific parameters and requirements.

