# Upload to URL: Publish HTML



```
POST https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/publish-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upload to URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/publish-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlCode": "string",
  "pagePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/publish-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlCode": "string",
    "pagePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlCode` | string | yes | Raw HTML code to publish. |
| `pagePath` | string | yes | Public path for the published page (for example: my-landing-page). |
| `subdomain` | string | no | Optional subdomain name. |
| `expiryDays` | string | no | Optional number of days before the published page expires. Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "message": "string",
      "page_path": "string",
      "pretty_url": "https://example.com",
      "status": "string",
      "subdomain": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `message` | string |  |
| `page_path` | string |  |
| `pretty_url` | string |  |
| `status` | string |  |
| `subdomain` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Upload to URL API, this operation is `POST /api/publish` (base URL `https://uploadtourl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-html.md) for the provider-specific parameters and requirements.

