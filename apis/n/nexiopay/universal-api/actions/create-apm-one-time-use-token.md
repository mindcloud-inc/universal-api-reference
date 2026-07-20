# Nexiopay: Create APM one-time-use token



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-apm-one-time-use-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-apm-one-time-use-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-apm-one-time-use-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | APM transaction data object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerRedirectUrl": "https://example.com",
      "expiration": "2026-05-07T12:00:00.000Z",
      "redirectUrls": [
        {}
      ],
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerRedirectUrl` | string | Customer redirect URL. |
| `expiration` | date | Token expiration timestamp. |
| `redirectUrls` | array<object> | APM redirect URLs. |
| `token` | string | APM one-time-use token. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /apm/v3/token` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-apm-one-time-use-token.md) for the provider-specific parameters and requirements.

