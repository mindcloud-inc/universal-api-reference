# Wayback Machine: Search CDX Captures

Finds archived captures in the Wayback Machine CDX index.

```
GET https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/search-cdx-captures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayback Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/search-cdx-captures?connectionId=$CONNECTION_ID&url=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/search-cdx-captures?${params}`, {
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
| `url` | string | yes | URL, host, prefix, or domain to search in the CDX capture index. Example: `example.com`. |
| `limit` | number | no | Maximum number of CDX rows to return. Default: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `matchType` | list | no | Optional URL match scope: exact, prefix, host, or domain. One of: `0`, `1`, `2`, `3`. Example: `exact`. |
| `from` | string | no | Optional inclusive start timestamp, using 1 to 14 digits in yyyyMMddhhmmss order. Example: `2010`. |
| `to` | string | no | Optional inclusive end timestamp, using 1 to 14 digits in yyyyMMddhhmmss order. Example: `2011`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "captures": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `captures` | array<array> | CDX JSON array. First row contains field names; subsequent rows contain capture values in that order. |

## Native endpoint

Through the native Wayback Machine API, this operation is `GET https://web.archive.org/cdx/search/cdx` (base URL `https://archive.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cdx-captures.md) for the provider-specific parameters and requirements.

