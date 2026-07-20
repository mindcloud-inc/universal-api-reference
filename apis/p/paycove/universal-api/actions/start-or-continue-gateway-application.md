# Paycove: Start Or Continue Gateway Application

Starts or continues a gateway application in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/start-or-continue-gateway-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/start-or-continue-gateway-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uniqueAccountId": "c992329175ebd88509430024bcaba5da"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/start-or-continue-gateway-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uniqueAccountId": "c992329175ebd88509430024bcaba5da"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uniqueAccountId` | string | yes | Paycove account unique_id. Example: `c992329175ebd88509430024bcaba5da`. |
| `firstName` | string | no | Override admin user's first name. Example: `Jane`. |
| `lastName` | string | no | Override admin user's last name. Example: `Doe`. |
| `company` | string | no | Override company name for the application. Example: `Example Company`. |
| `redirectUrl` | string | no | Custom redirect URL after the application. Example: `https://example.com/redirect`. |
| `completeUrl` | string | no | Custom completion URL. Example: `https://example.com/complete`. |
| `refreshUrl` | string | no | Custom refresh URL. Example: `https://example.com/refresh`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `GET https://paycove.io/continue-gateway-application/:unique_account_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-or-continue-gateway-application.md) for the provider-specific parameters and requirements.

