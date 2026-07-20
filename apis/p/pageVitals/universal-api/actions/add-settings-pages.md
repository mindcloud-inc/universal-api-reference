# PageVitals: Add Settings Pages



```
POST https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-settings-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-settings-pages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "input[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-settings-pages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "input[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes |  |
| `input[].url` | string | yes |  |
| `input[].alias` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "id": "string",
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
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `POST /:websiteId/settings/pages` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-settings-pages.md) for the provider-specific parameters and requirements.

