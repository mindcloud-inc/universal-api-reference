# Writeathon: Get Card By ID

Retrieves a Writeathon card by ID.

```
GET https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-card-by-id?${params}`, {
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
| `id` | string | yes | The Writeathon card ID to retrieve. |

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

Through the native Writeathon API, this operation is `POST /v1/users/{{credentials.userId}}/cards/get` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-by-id.md) for the provider-specific parameters and requirements.

