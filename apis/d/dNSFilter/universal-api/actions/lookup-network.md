# DNSFilter: Lookup Network



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-network
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-network?connectionId=$CONNECTION_ID&requestingIpAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestingIpAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-network?${params}`, {
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
| `requestingIpAddress` | string | yes | Requesting IP address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_default_appearance": true,
      "block_email_addr": "ava@example.com",
      "block_logo_uuid": "string",
      "block_org_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_default_appearance` | boolean |  |
| `block_email_addr` | string |  |
| `block_logo_uuid` | string |  |
| `block_org_name` | string |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/networks/lookup` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-network.md) for the provider-specific parameters and requirements.

