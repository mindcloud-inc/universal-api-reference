# Flow App: Create Registrant



```
POST https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-registrant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-registrant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "eventSessionToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-registrant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "eventSessionToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The attendee email address to register. |
| `firstName` | string | yes | The attendee first name. |
| `lastName` | string | yes | The attendee last name. |
| `eventSessionToken` | string | yes | The target event session token. |
| `redirect` | boolean | no | Optional SSO-style redirect flag documented by Flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "id": 1,
      "isNew": true,
      "passCode": 1,
      "time": "string",
      "timezone": "string",
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `id` | number |  |
| `isNew` | boolean |  |
| `passCode` | number |  |
| `time` | string |  |
| `timezone` | string |  |
| `token` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Flow App API, this operation is `POST /registrants` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-registrant.md) for the provider-specific parameters and requirements.

