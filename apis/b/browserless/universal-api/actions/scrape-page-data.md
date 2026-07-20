# Browserless: Scrape Page Data

Retrieves structured page data from Browserless using selectors.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/scrape-page-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/scrape-page-data?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&elements%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "elements[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/scrape-page-data?${params}`, {
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
| `url` | string | yes | The URL to scrape for structured data extraction. |
| `elements[]` | array<object> | yes | Array of selector objects that define the data to extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | Structured scrape results for each requested selector block. |

## Native endpoint

Through the native Browserless API, this operation is `POST /scrape` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-page-data.md) for the provider-specific parameters and requirements.

