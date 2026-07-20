# DNSFilter: Get Domain Note



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-domain-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-domain-note?connectionId=$CONNECTION_ID&resource=string&id=1&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resource": "string",
  "id": "1",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-domain-note?${params}`, {
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
| `resource` | string | yes | Valid resources: policies, msps or organizations |
| `id` | number | yes | Resource ID |
| `domain` | string | yes | Domain |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_notes": {},
      "block_notes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_notes` | object |  |
| `block_notes` | object |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/notes/:resource/:id/:domain` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-note.md) for the provider-specific parameters and requirements.

