# Wayback Machine: Get CDX Page Count

Retrieves the CDX result page count for a Wayback query.

```
GET https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-cdx-page-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayback Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-cdx-page-count?connectionId=$CONNECTION_ID&url=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-cdx-page-count?${params}`, {
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
| `url` | string | yes | URL, host, prefix, or domain to estimate CDX result pages for. Example: `example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Optional CDX page size block count for page-count estimation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageCount` | number | Number of CDX pagination pages reported by showNumPages=true. |

## Native endpoint

Through the native Wayback Machine API, this operation is `GET https://web.archive.org/cdx/search/cdx` (base URL `https://archive.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cdx-page-count.md) for the provider-specific parameters and requirements.

