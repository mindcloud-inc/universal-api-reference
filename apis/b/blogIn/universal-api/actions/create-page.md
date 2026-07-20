# BlogIn: Create Page

Creates a new page in BlogIn.

```
POST https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "author.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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

Through the native BlogIn API, this operation is `POST /pages` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

