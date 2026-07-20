# Evoliz: Create Client Contact

Creates a new client contact in Evoliz.

```
POST https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "civility": "string",
      "client": {
        "clientid": 1,
        "code": "string",
        "name": "Ava Chen"
      },
      "consent": "string",
      "contactid": 1,
      "email": "ava@example.com",
      "enabled": true,
      "favorite": true,
      "firstname": "Ava",
      "lastname": "Chen",
      "userid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `civility` | string |  |
| `client.clientid` | number |  |
| `client.code` | string |  |
| `client.name` | string |  |
| `consent` | string |  |
| `contactid` | number |  |
| `email` | string |  |
| `enabled` | boolean |  |
| `favorite` | boolean |  |
| `firstname` | string |  |
| `lastname` | string |  |
| `userid` | number |  |

## Native endpoint

Through the native Evoliz API, this operation is `POST /api/v1/contacts-clients` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-contact.md) for the provider-specific parameters and requirements.

