# Synchroteam: Get User Detail

Retrieves a user from Synchroteam by supported identifier.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-user-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&identifierType=string&identifierValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifierType": "string",
  "identifierValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-user-detail?${params}`, {
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
| `identifierType` | string | yes | Which identifier to use (for example: login, id). |
| `identifierValue` | string | yes | The identifier value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "language": "string",
      "lastName": "Chen",
      "login": "string",
      "profile": "string",
      "startLocation": {
        "fullAdress": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `language` | string |  |
| `lastName` | string |  |
| `login` | string |  |
| `profile` | string |  |
| `startLocation.fullAdress` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/User/Details` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-detail.md) for the provider-specific parameters and requirements.

