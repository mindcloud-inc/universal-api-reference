# Aqara Home for SG: Refresh Access Token

Refreshes access and refresh tokens in Aqara Home for SG.

```
PUT https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/refresh-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/refresh-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refreshToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/refresh-access-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refreshToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | yes | Aqara refresh token returned by Get Access Token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresIn": "string",
      "openId": "string",
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `expiresIn` | string |  |
| `openId` | string |  |
| `refreshToken` | string |  |

## Native endpoint

Through the native Aqara Home for SG API, this operation is `POST /v3.0/open/api` (base URL `https://open-sg.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-access-token.md) for the provider-specific parameters and requirements.

