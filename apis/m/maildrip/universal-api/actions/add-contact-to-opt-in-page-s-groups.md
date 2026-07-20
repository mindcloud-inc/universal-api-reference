# Maildrip: Add contact to opt-in page's groups



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-contact-to-opt-in-page-s-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-contact-to-opt-in-page-s-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-contact-to-opt-in-page-s-groups', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | ID of the opt-in page to add contact to its groups |
| `email` | string | yes | Email of the contact |
| `name` | string | no | Full name of the contact |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "message": "string",
      "post_signup_config": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | Updated contact data |
| `message` | string | Success message |
| `post_signup_config` | object | Post-signup redirect/message configuration for the opt-in page (null when not configured) |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/opt-in-pages/{pageId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-opt-in-page-s-groups.md) for the provider-specific parameters and requirements.

