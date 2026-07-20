# Pushbullet: Delete Subscription

Deletes an existing subscription from Pushbullet.

```
DELETE https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&iden=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iden": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-subscription?${params}`, {
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
| `iden` | string | yes | Subscription identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Pushbullet API, this operation is `DELETE /subscriptions/:iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.

