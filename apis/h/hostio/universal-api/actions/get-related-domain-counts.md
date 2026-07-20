# Host.io: Get Related Domain Counts

Retrieves related domain counts from Host.io.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-related-domain-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-related-domain-counts?connectionId=$CONNECTION_ID&domain=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "google.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-related-domain-counts?${params}`, {
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
| `domain` | string | yes | Domain to retrieve related-domain counts for. Default: `google.com`. Example: `google.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": [
        {}
      ],
      "backlinks": [
        {}
      ],
      "ip": [
        {}
      ],
      "mx": [
        {}
      ],
      "ns": [
        {}
      ],
      "redirects": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | array<object> | ASN values and counts. |
| `backlinks` | array<object> | Backlink target values and counts. |
| `ip` | array<object> | Related IP values and counts. |
| `mx` | array<object> | MX values and counts. |
| `ns` | array<object> | NS values and counts. |
| `redirects` | array<object> | Redirect target values and counts. |

## Native endpoint

Through the native Host.io API, this operation is `GET /related/:domain` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-domain-counts.md) for the provider-specific parameters and requirements.

