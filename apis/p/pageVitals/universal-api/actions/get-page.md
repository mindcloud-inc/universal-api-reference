# PageVitals: Get Page



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page?connectionId=$CONNECTION_ID&websiteId=string&pageId=string&device=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "pageId": "string",
  "device": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page?${params}`, {
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
| `websiteId` | string | yes | The internal ID of the website. |
| `pageId` | string | yes | The internal ID of the page. |
| `device` | string | yes | The device profile to query, such as desktop or mobile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "device": "string",
      "id": "string",
      "latestMetrics": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `device` | string |  |
| `id` | string |  |
| `latestMetrics` | object |  |
| `url` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/pages/:pageId` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

