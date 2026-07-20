# Trello: Get List

Retrieves a list from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-list?${params}`, {
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
| `id` | string | yes | List identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "id": "string",
      "idBoard": "string",
      "name": "Ava Chen",
      "pos": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `id` | string |  |
| `idBoard` | string |  |
| `name` | string |  |
| `pos` | number |  |

## Native endpoint

Through the native Trello API, this operation is `GET lists/:id` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

