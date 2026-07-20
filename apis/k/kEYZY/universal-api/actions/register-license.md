# KEYZY: Register License

Registers a new customer to a KEYZY license.

```
POST https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/register-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/register-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "skuNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/register-license', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "skuNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Licensee's email address. |
| `endAt` | number | no | License end time as a Unix timestamp. |
| `name` | string | yes | Licensee's name. |
| `skuNumber` | string | yes | A sku_number. |
| `startAt` | number | no | License start time as a Unix timestamp. |
| `type` | string | no | License type: perpetual, subscription, or trial. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {
        "serial": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message.serial` | string | Created license serial number. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/register` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-license.md) for the provider-specific parameters and requirements.

