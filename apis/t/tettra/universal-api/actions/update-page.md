# Tettra: Update Page

Updates an existing page in Tettra.

```
PUT https://connect.mindcloud.co/v1/universal/tettra/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tettra/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Replacement page content formatted as HTML. |
| `categoryId` | number | no | Updated category ID. |
| `ownerId` | number | no | Updated owner of the page. |
| `pageId` | number | yes | Page ID to update. |
| `subcategoryId` | number | no | Updated subcategory ID. |
| `title` | string | no | Updated page title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "pageId": 1,
      "pageUrl": "https://example.com",
      "revisionId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `pageId` | number |  |
| `pageUrl` | string |  |
| `revisionId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tettra API, this operation is `PATCH /teams/85329/pages/:page_id` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

