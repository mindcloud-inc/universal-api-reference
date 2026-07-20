# Go4Clients: Validate 2FA Challenge

Validates a Go4Clients two-factor authentication code.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/validate2-fa-challenge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/validate2-fa-challenge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "application": "MindCloud",
  "key": "57311224477",
  "code": "1700"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/validate2-fa-challenge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "application": "MindCloud",
    "key": "57311224477",
    "code": "1700"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `application` | string | yes | Application that created the two-factor authentication challenge. Example: `MindCloud`. |
| `key` | string | yes | Telephone number or key associated with the challenge. Example: `57311224477`. |
| `code` | string | yes | Code to validate. Example: `1700`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | boolean | Whether the submitted 2FA code is valid. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/tfa/v1.0/validate` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate2-fa-challenge.md) for the provider-specific parameters and requirements.

