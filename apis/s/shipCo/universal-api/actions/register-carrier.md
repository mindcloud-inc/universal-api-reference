# Ship&Co: Register Carrier



```
POST https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-carrier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-carrier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "credentials": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-carrier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "credentials": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Carrier type such as dhl, fedex, japanpost, sagawa, yamato, yuupack, yuupacket, yuumail, or seino. |
| `credentials` | object | yes | Carrier credentials object. Required fields vary by carrier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings` | object | no | Carrier settings object, including print settings where required. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "settings": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | string |  |
| `settings` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /carriers` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-carrier.md) for the provider-specific parameters and requirements.

