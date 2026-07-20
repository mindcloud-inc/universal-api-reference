# IPLocate: Lookup Privacy



```
GET https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-privacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPLocate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-privacy?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-privacy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | string | yes | IPv4 or IPv6 address to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_abuser": true,
      "is_anonymous": true,
      "is_bogon": true,
      "is_hosting": true,
      "is_icloud_relay": true,
      "is_proxy": true,
      "is_tor": true,
      "is_vpn": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_abuser` | boolean |  |
| `is_anonymous` | boolean |  |
| `is_bogon` | boolean |  |
| `is_hosting` | boolean |  |
| `is_icloud_relay` | boolean |  |
| `is_proxy` | boolean |  |
| `is_tor` | boolean |  |
| `is_vpn` | boolean |  |

## Native endpoint

Through the native IPLocate API, this operation is `GET /lookup/:ip/privacy` (base URL `https://iplocate.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-privacy.md) for the provider-specific parameters and requirements.

