# LoopedIn: Delete Roadmap Card

Deletes an existing roadmap card from LoopedIn.

```
DELETE https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/delete-roadmap-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/delete-roadmap-card?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/delete-roadmap-card?${params}`, {
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
| `id` | string | yes | The LoopedIn roadmap card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native LoopedIn API, this operation is `DELETE /roadmap-cards/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-roadmap-card.md) for the provider-specific parameters and requirements.

