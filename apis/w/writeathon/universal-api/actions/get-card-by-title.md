# Writeathon: Get Card By Title

Retrieves a Writeathon card by title.

```
GET https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-title?connectionId=$CONNECTION_ID&title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-title?${params}`, {
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
| `title` | string | yes | The exact Writeathon card title to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "content": "string",
        "created": "string",
        "id": "string",
        "title": "string",
        "updated": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.content` | string |  |
| `data.created` | string |  |
| `data.id` | string |  |
| `data.title` | string |  |
| `data.updated` | string |  |

## Native endpoint

Through the native Writeathon API, this operation is `POST /v1/users/{{credentials.userId}}/cards/get` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-by-title.md) for the provider-specific parameters and requirements.

