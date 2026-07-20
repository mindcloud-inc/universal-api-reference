# BlogIn: Update Page

Updates an existing page in BlogIn.

```
PUT https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "title": "string",
  "author.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "title": "string",
    "author.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the page to update. |
| `title` | string | yes | The title of the page. |
| `text` | string | no | The HTML text of the page. |
| `author.id` | number | yes | The ID of the author of the page. |
| `published` | boolean | no | Whether the page is published. |
| `position` | number | no | The sort position of the page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "id": 1,
      "position": 1,
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `id` | number |  |
| `position` | number |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native BlogIn API, this operation is `POST /pages/:id` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

