# Trello: Get Card

Retrieves a card from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-card?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-card?${params}`, {
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
      "dateLastActivity": "string",
      "desc": "string",
      "id": "string",
      "idBoard": "string",
      "idList": "string",
      "idMembers": [
        "string"
      ],
      "labels": [
        "string"
      ],
      "name": "Ava Chen",
      "shortUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `dateLastActivity` | string |  |
| `desc` | string |  |
| `id` | string |  |
| `idBoard` | string |  |
| `idList` | string |  |
| `idMembers[]` | string |  |
| `labels[]` | string |  |
| `name` | string |  |
| `shortUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Trello API, this operation is `GET cards/:id` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card.md) for the provider-specific parameters and requirements.

