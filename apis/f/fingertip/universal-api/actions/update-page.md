# Fingertip: Update Page



```
PUT https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Description of the page content, can be null |
| `name` | string | no | Name of the page, can be null |
| `pageId` | string | yes | ID of the page to update |
| `position` | number | no | Display position of the page within the site |
| `siteId` | string | no | ID of the site this page belongs to |
| `slug` | string | no | URL-friendly path segment for the page |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `PATCH /v1/pages/:pageId` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

