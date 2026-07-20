# Engage: Remove Subscriber from List

Removes a subscriber from an Engage list.

```
DELETE https://connect.mindcloud.co/v1/universal/engage/latest/actions/remove-subscriber-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/engage/latest/actions/remove-subscriber-from-list?connectionId=$CONNECTION_ID&id=string&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/remove-subscriber-from-list?${params}`, {
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
| `id` | string | yes | The Engage list ID. |
| `uid` | string | yes | The subscriber user ID from your application. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Status returned after the subscriber is removed from the list. |

## Native endpoint

Through the native Engage API, this operation is `DELETE /lists/:id/subscribers/:uid` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subscriber-from-list.md) for the provider-specific parameters and requirements.

