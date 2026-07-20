# Big Cartel: Update Page

Updates an existing page in Big Cartel.

```
PUT https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "pageId": "string",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "pageId": "string",
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Big Cartel account ID. |
| `pageId` | string | yes | The Big Cartel page ID. |
| `id` | string | yes |  |
| `name` | string | yes |  |
| `content` | string | no |  |
| `useLayout` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "category": "string",
        "content": "string",
        "isPublished": true,
        "name": "Ava Chen",
        "path": "string",
        "useLayout": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.category` | string |  |
| `attributes.content` | string |  |
| `attributes.isPublished` | boolean |  |
| `attributes.name` | string |  |
| `attributes.path` | string |  |
| `attributes.useLayout` | boolean |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `PATCH /v1/accounts/[:account-id]/pages/[:page-id]` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

