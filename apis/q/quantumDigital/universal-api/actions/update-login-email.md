# Quantum Digital: Update Login Email



```
PUT https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/update-login-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/update-login-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currentPassword": "string",
  "newEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/update-login-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currentPassword": "string",
    "newEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentPassword` | string | yes |  |
| `newEmail` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorField": "string",
      "errorMsg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorField` | string | Field associated with a validation error. |
| `errorMsg` | string | Error message returned by the provider. |
| `success` | boolean | Whether the login email was updated successfully. |

## Native endpoint

Through the native Quantum Digital API, this operation is `PUT /devplatform/accounts/:dashboardAccountId/email` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-login-email.md) for the provider-specific parameters and requirements.

