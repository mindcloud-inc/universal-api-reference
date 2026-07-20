# Trello: Remove Member from Card

Removes a member from a Trello card.

```
DELETE https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-member-from-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-member-from-card?connectionId=$CONNECTION_ID&id=string&idMember=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "idMember": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-member-from-card?${params}`, {
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
| `idMember` | string | yes | Member identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullName": "Ava Chen",
      "id": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullName` | string |  |
| `id` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Trello API, this operation is `DELETE cards/:id/idMembers/:idMember` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-member-from-card.md) for the provider-specific parameters and requirements.

