# Trello: Get Attachments on a Card

Retrieves attachments on a card from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-attachments-on-a-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-attachments-on-a-card?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-attachments-on-a-card?${params}`, {
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
| `id` | string | yes | Card identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "idMember": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `idMember` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Trello API, this operation is `GET cards/:id/attachments` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachments-on-a-card.md) for the provider-specific parameters and requirements.

