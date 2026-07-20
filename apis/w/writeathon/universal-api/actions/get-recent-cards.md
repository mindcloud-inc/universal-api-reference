# Writeathon: Get Recent Cards

Retrieves recently updated cards from Writeathon.

```
GET https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-recent-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-recent-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-recent-cards?${params}`, {
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
| `excludeDateTitle` | boolean | no | Exclude system-generated date titles from the recent cards list. |
| `space` | string | no | Optional Writeathon space ID. Leave blank to use the default space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "title": "string"
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
| `data[].id` | string |  |
| `data[].title` | string |  |

## Native endpoint

Through the native Writeathon API, this operation is `GET /v1/users/{{credentials.userId}}/cards/recent` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recent-cards.md) for the provider-specific parameters and requirements.

