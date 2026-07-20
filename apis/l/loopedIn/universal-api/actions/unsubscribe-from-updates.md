# LoopedIn: Unsubscribe from Updates

Unsubscribes a user from updates in LoopedIn.

```
DELETE https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/unsubscribe-from-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/unsubscribe-from-updates?connectionId=$CONNECTION_ID&email=ava%40example.com&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/unsubscribe-from-updates?${params}`, {
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
| `email` | string | yes | The subscriber email address. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productGuid": "string",
      "success": true,
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productGuid` | string |  |
| `success` | boolean |  |
| `unsubscribed` | boolean |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /updates/public-unsubscribe` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-from-updates.md) for the provider-specific parameters and requirements.

