# Trello: Get Lists on a Board

Retrieves lists on a board from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-lists-on-a-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-lists-on-a-board?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-lists-on-a-board?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "color": {},
      "datasource": {
        "filter": true
      },
      "id": "string",
      "idBoard": "string",
      "name": "Ava Chen",
      "pos": 1,
      "softLimit": {},
      "subscribed": true,
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `color` | object |  |
| `datasource.filter` | boolean |  |
| `id` | string |  |
| `idBoard` | string |  |
| `name` | string |  |
| `pos` | number |  |
| `softLimit` | object |  |
| `subscribed` | boolean |  |
| `type` | object |  |

## Native endpoint

Through the native Trello API, this operation is `GET boards/:id/lists` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lists-on-a-board.md) for the provider-specific parameters and requirements.

