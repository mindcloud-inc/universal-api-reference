# Moodo & Moodo AIR: Register Box Serial

Registers a Moodo box serial to the current account.

```
PUT https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/register-box-serial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/register-box-serial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/register-box-serial', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceKey": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceKey` | number |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `PATCH /boxes` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-box-serial.md) for the provider-specific parameters and requirements.

