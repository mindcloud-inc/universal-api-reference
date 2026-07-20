# Evoliz: List Client Contacts

Retrieves client contacts from Evoliz.

```
GET https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-client-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-client-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-client-contacts?${params}`, {
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
| `clientId` | number | no | Optional filter for one client. |

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

Through the native Evoliz API, this operation is `GET /api/v1/contacts-clients` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-contacts.md) for the provider-specific parameters and requirements.

