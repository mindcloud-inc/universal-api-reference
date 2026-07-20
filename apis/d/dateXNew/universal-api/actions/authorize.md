# DateX: Authorize



```
POST https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/authorize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/authorize" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/authorize', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | Azure client ID. Default: `{{credentials.clientId}}`. |
| `clientSecret` | string | no | Azure client secret. Default: `{{credentials.clientSecret}}`. |
| `grantType` | string | no | OAuth grant type. Default: `client_credentials`. |
| `scope` | string | no | Azure token scope. Default: `{{credentials.scope}}`. |
| `url` | string | no | Token URL. Default: `{{credentials.tokenUrl}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresIn": 1,
      "extExpiresIn": 1,
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `expiresIn` | number |  |
| `extExpiresIn` | number |  |
| `tokenType` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST https://login.microsoftonline.com/6498fd5a-7169-49a0-a87e-2107759e83e2/oauth2/v2.0/token` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize.md) for the provider-specific parameters and requirements.

