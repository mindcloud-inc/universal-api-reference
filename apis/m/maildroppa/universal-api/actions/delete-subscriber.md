# Maildroppa: Delete Subscriber

Deletes a subscriber from Maildroppa by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber?${params}`, {
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
| `subscriberId` | string | yes | UUID of the subscriber. |

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
| `success` | boolean | True when delete subscriber completed. |

## Native endpoint

Through the native Maildroppa API, this operation is `DELETE /subscribers/{subscriberId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

