# Writeathon: Get Writing Picks

Retrieves writing picks from the current Writeathon account.

```
GET https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-writing-picks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-writing-picks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-writing-picks?${params}`, {
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
| `type` | string | no | Optional writing-pick scope: all, page, or card. Default: `all`. |
| `limit` | number | no | How many writing picks to return, from 1 to 10. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "content": "string",
          "created": "string",
          "id": "string",
          "title": "string",
          "type": "string",
          "updated": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].content` | string |  |
| `data[].created` | string |  |
| `data[].id` | string |  |
| `data[].title` | string |  |
| `data[].type` | string |  |
| `data[].updated` | string |  |

## Native endpoint

Through the native Writeathon API, this operation is `POST /v1/users/{{credentials.userId}}/writing-pick` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-writing-picks.md) for the provider-specific parameters and requirements.

