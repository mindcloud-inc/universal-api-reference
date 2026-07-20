# EMnify: Create Application Token

Creates a new application token in EMnify.

```
POST https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-application-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-application-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-application-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "Paste the auth_token from Retrieve Authentication Token"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `description` | string | no | Description for the new application token. Example: `MindCloud disposable app token`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiryDate` | string | no | Expiry date with optional time and time zone. Example: `2026-03-27T18:00:00+0000`. |
| `ip` | string | no | Allowed IP address in CIDR notation. Example: `203.0.113.0/24`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationToken` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `POST /application_token` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-application-token.md) for the provider-specific parameters and requirements.

