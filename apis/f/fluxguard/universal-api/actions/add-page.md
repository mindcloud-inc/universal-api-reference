# Fluxguard: Add Page

Adds a new page for monitoring in Fluxguard.

```
POST https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/add-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/add-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/add-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL to monitor. |
| `siteId` | string | no | Existing site identifier to attach the page to. |
| `sessionId` | string | no | Existing session identifier to attach the page to. |
| `categoryId` | string | no | Category ID for the new site when creating one. |
| `categoryName` | string | no | Category name for the new site when creating one. |
| `siteNickname` | string | no | Nickname for the new site. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageId": "string",
      "sessionId": "string",
      "siteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageId` | string | Identifier of the newly added page. |
| `sessionId` | string | Identifier of the session containing the added page. |
| `siteId` | string | Identifier of the site containing the added page. |

## Native endpoint

Through the native Fluxguard API, this operation is `POST /add-page` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-page.md) for the provider-specific parameters and requirements.

