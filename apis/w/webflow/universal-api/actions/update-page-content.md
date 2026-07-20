# Webflow: Update Page Content

Updates static page content in Webflow.

```
PUT https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "localeId": "string",
  "nodes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "localeId": "string",
    "nodes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | Unique identifier of the page. |
| `localeId` | string | yes | Locale identifier for the content update target. |
| `nodes[]` | array<object> | yes | Updated DOM nodes payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Validation or publish errors returned by the update page content request. |

## Native endpoint

Through the native Webflow API, this operation is `POST /pages/:page_id/dom` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-content.md) for the provider-specific parameters and requirements.

