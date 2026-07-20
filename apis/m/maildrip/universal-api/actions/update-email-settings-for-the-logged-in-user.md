# Maildrip: Update email settings for the logged-in user



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-settings-for-the-logged-in-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-settings-for-the-logged-in-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-settings-for-the-logged-in-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailFrom` | string | no |  |
| `emailReplyTo` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/users/email-settings` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-settings-for-the-logged-in-user.md) for the provider-specific parameters and requirements.

