# BigDataCloud: List ASN Ranks

Retrieves ASN rank data from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-asn-ranks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-asn-ranks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-asn-ranks?${params}`, {
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
| `batchSize` | number | no | Requested batch size. Maximum value is 1000. Example: `10`. |
| `offset` | number | no | Number of entries to skip. Default: `0`. Example: `0`. |
| `sort` | string | no | Sort response by rank, asn, asnNumeric, organisation, or countryCode. Default: `rank`. Example: `rank`. |
| `order` | string | no | Sort order: asc or desc. Default: `asc`. Example: `asc`. |
| `localityLanguage` | string | no | Preferred language for localized country names. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asns": [
        {}
      ],
      "batch": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asns` | array<object> | Array of ASN rank entries returned for the current batch. |
| `batch` | number | Number of entries in the current batch. |
| `offset` | number | Number of entries skipped. |
| `total` | number | Total number of entries available. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/asn-rank-list` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asn-ranks.md) for the provider-specific parameters and requirements.

