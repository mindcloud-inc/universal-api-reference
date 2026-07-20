# Maildrip: Identify a contact and sync attributes from your app



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/identify-a-contact-and-sync-attributes-from-your-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/identify-a-contact-and-sync-attributes-from-your-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/identify-a-contact-and-sync-attributes-from-your-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The contact's email address (used as the unique identifier) |
| `firstName` | string | no | Contact's first name |
| `lastName` | string | no | Contact's last name |
| `traits` | object | no | Arbitrary key-value attributes from your app to store on the contact. Keys must be alphanumeric with underscores/hyphens (max 50 chars). Values must be primitives: string, number, or boolean (max 500 chars each). Maximum 10 traits per call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/identify` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-a-contact-and-sync-attributes-from-your-app.md) for the provider-specific parameters and requirements.

