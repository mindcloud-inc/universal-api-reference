# Aqara Home for SG: Request Auth Code

Requests an authorization code from Aqara Home for SG.

```
POST https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/request-auth-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/request-auth-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/request-auth-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | Aqara account email or phone number that should receive the auth code. |
| `accessTokenValidity` | string | no | Optional token validity such as 1h, 1d, or 7d. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authCode` | string |  |

## Native endpoint

Through the native Aqara Home for SG API, this operation is `POST /v3.0/open/api` (base URL `https://open-sg.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-auth-code.md) for the provider-specific parameters and requirements.

