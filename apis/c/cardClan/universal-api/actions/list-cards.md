# CardClan: List Cards

Retrieves cards from a CardClan workspace.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards?connectionId=$CONNECTION_ID&workspace=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards?${params}`, {
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
| `workspace` | string | yes | Workspace identifier used to retrieve cards. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "choices": [
        {}
      ],
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Owning CardClan user ID for the card choice set. |
| `choices` | array<object> | Available card choices for the workspace. |
| `key` | string | Response group key. |

## Native endpoint

Through the native CardClan API, this operation is `POST /integration/cards` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

