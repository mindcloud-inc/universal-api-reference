# ProProfs Project: Get Client

Retrieves a client from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes | The client ID to fetch. |

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

Through the native ProProfs Project API, this operation is `GET /clients/{{client_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

