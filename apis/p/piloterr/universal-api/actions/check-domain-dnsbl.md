# Piloterr: Check Domain DNSBL



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-dnsbl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-dnsbl?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/check-domain-dnsbl?${params}`, {
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
| `query` | string | yes | Domain or IP address to check against DNSBL providers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listed": true,
      "query": "string",
      "sources": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listed` | boolean |  |
| `query` | string |  |
| `sources` | array<string> |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /domain/dnsbl` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-dnsbl.md) for the provider-specific parameters and requirements.

