# Framework360: Login User



```
POST https://connect.mindcloud.co/v1/universal/framework360/latest/actions/login-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/login-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loginEmail": "ava@example.com",
  "loginPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/login-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loginEmail": "ava@example.com",
    "loginPassword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loginEmail` | string | yes | Backoffice user email. |
| `loginPassword` | string | yes | Backoffice user password. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "active": 1,
      "avatar": "string",
      "cognome": "string",
      "email": "ava@example.com",
      "formatted_name": "Ava Chen",
      "has_wizard": 1,
      "id": "string",
      "nome": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `active` | number |  |
| `avatar` | string |  |
| `cognome` | string |  |
| `email` | string |  |
| `formatted_name` | string |  |
| `has_wizard` | number |  |
| `id` | string |  |
| `nome` | string |  |

## Native endpoint

Through the native Framework360 API, this operation is `POST users/login` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-user.md) for the provider-specific parameters and requirements.

