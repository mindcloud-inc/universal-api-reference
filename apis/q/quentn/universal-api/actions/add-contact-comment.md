# Quentn: Add Contact Comment



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "123",
  "comment": "Reached out after webinar signup"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "123",
    "comment": "Reached out after webinar signup"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Numeric Quentn contact id. Example: `123`. |
| `comment` | string | yes | Comment text to add to the contact. Example: `Reached out after webinar signup`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string | The id of the created Quentn contact comment. |
| `success` | boolean | Whether Quentn accepted the comment create request. |

## Native endpoint

Through the native Quentn API, this operation is `POST /contact/:contact_id/comments` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-comment.md) for the provider-specific parameters and requirements.

