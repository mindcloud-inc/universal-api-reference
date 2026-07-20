# GMass: Remove Account Unsubscribe

Deletes an address from your GMass unsubscribe list.

```
DELETE https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-account-unsubscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-account-unsubscribe?connectionId=$CONNECTION_ID&emailAddress=gmass-stage3%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "gmass-stage3@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-account-unsubscribe?${params}`, {
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
| `emailAddress` | string | yes | Email address to remove from the account unsubscribe list. Example: `gmass-stage3@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com",
      "sender": "string",
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string | Email address removed from the account unsubscribe list. |
| `sender` | string | Sender associated with the unsubscribe record when available. |
| `unsubscribeTime` | date | Time on the unsubscribe record returned by GMass. |

## Native endpoint

Through the native GMass API, this operation is `DELETE /unsubscribes` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-account-unsubscribe.md) for the provider-specific parameters and requirements.

