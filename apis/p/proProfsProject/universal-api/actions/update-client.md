# ProProfs Project: Update Client

Updates an existing client in ProProfs Project.

```
PUT https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The client ID to update. |
| `clientName` | string | no | The updated client name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "address": "string",
      "background": "string",
      "city": "string",
      "clientId": "string",
      "clientName": "Ava Chen",
      "contactId": "string",
      "country": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "email": "ava@example.com",
      "fax": "string",
      "mobile": "string",
      "postcode": "string",
      "state": "string",
      "tel": "string",
      "userId": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `address` | string |  |
| `background` | string |  |
| `city` | string |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `contactId` | string |  |
| `country` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `mobile` | string |  |
| `postcode` | string |  |
| `state` | string |  |
| `tel` | string |  |
| `userId` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `PUT /clients/{{client_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

