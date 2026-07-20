# Host.io: List Domains by ASN

Finds domains in Host.io by ASN.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-asn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-asn?connectionId=$CONNECTION_ID&limit=25&offset=0&value=AS15169" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "value": "AS15169"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-asn?${params}`, {
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
| `value` | string | yes | ASN to search domains by. Default: `AS15169`. Example: `AS15169`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": "string",
      "domains": [
        "string"
      ],
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | string | ASN searched. |
| `domains` | array<string> | Domains associated with the ASN. |
| `page` | number | Current result page. |
| `total` | number | Total available result count. |

## Native endpoint

Through the native Host.io API, this operation is `GET /domains/asn/:value` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains-by-asn.md) for the provider-specific parameters and requirements.

