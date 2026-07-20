# SMSup: Create Subaccount



```
POST https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/create-subaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/create-subaccount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "new_subaccount_user_name",
  "email": "user@example.com",
  "name": "John",
  "surname": "Doe",
  "password": "secure-password",
  "language": "es"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/create-subaccount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "new_subaccount_user_name",
    "email": "user@example.com",
    "name": "John",
    "surname": "Doe",
    "password": "secure-password",
    "language": "es"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | yes | Username for the subaccount. Example: `new_subaccount_user_name`. |
| `email` | string | yes | Email for the subaccount. Example: `user@example.com`. |
| `name` | string | yes | First name of the subaccount user. Example: `John`. |
| `surname` | string | yes | Surname of the subaccount user. Example: `Doe`. |
| `password` | string | yes | Password for the subaccount. Example: `secure-password`. |
| `language` | string | yes | Subaccount language. Example: `es`. |
| `enableShortener` | number | no | Set to 1 to enable shortener features on the subaccount. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "password": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `password` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/subaccount/create` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subaccount.md) for the provider-specific parameters and requirements.

