# ScrapeUnblocker: Get Page Source

Retrieves page source from ScrapeUnblocker.

```
GET https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeUnblocker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeUnblocker/latest/actions/get-page-source?${params}`, {
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
| `url` | string | yes | The webpage URL to fetch. Example: `https://example.com`. |
| `proxyCountry` | string | no | Optional proxy country code. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | UTF-8 HTML bytes returned for the requested page. |
| `type` | string | Buffer wrapper type returned by the current RapidAPI runtime. |

## Native endpoint

Through the native ScrapeUnblocker API, this operation is `POST /getPageSource` (base URL `https://scrapeunblocker.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-source.md) for the provider-specific parameters and requirements.

