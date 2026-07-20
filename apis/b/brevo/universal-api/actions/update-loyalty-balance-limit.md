# Brevo: Update Loyalty Balance Limit



```
PUT https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-loyalty-balance-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-loyalty-balance-limit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bdid": "string",
  "blid": "string",
  "pid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-loyalty-balance-limit', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bdid": "string",
    "blid": "string",
    "pid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bdid` | string | yes |  |
| `blid` | string | yes |  |
| `pid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `PUT /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-loyalty-balance-limit.md) for the provider-specific parameters and requirements.

