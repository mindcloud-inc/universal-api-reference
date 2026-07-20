# DocRaptor: List DocRaptor IP Addresses

Retrieves the current DocRaptor IP addresses.

```
GET https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-docraptor-ip-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocRaptor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-docraptor-ip-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-docraptor-ip-addresses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ip` | string | DocRaptor outbound IP address. |

## Native endpoint

Through the native DocRaptor API, this operation is `GET https://docraptor.com/ips.json` (base URL `https://api.docraptor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-docraptor-ip-addresses.md) for the provider-specific parameters and requirements.

