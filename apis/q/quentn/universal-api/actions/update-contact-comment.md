# Quentn: Update Contact Comment



```
PUT https://connect.mindcloud.co/v1/universal/quentn/latest/actions/update-contact-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/update-contact-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "123",
  "commentId": "456",
  "comment": "Updated follow-up note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/update-contact-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "123",
    "commentId": "456",
    "comment": "Updated follow-up note"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Numeric Quentn contact id. Example: `123`. |
| `commentId` | number | yes | Existing comment id to update. Example: `456`. |
| `comment` | string | yes | Replacement comment text. Example: `Updated follow-up note`. |

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
| `success` | boolean | Whether Quentn accepted the comment update request. |

## Native endpoint

Through the native Quentn API, this operation is `PUT /contact/:contact_id/comments` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-comment.md) for the provider-specific parameters and requirements.

