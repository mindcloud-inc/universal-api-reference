# Wayback Machine: Get Oldest CDX Capture

Retrieves the oldest archived capture from the Wayback Machine CDX index.

```
GET https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-oldest-cdx-capture
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayback Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-oldest-cdx-capture?connectionId=$CONNECTION_ID&url=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-oldest-cdx-capture?${params}`, {
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
| `url` | string | yes | URL to find the oldest public CDX capture for. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capture": [
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
| `capture` | array<array> | CDX JSON array containing the header row and oldest capture row. |

## Native endpoint

Through the native Wayback Machine API, this operation is `GET https://web.archive.org/cdx/search/cdx` (base URL `https://archive.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oldest-cdx-capture.md) for the provider-specific parameters and requirements.

