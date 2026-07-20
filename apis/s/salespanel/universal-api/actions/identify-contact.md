# Salespanel: Identify Contact

Identifies a contact in Salespanel by associating an email.

```
PUT https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/identify-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/identify-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/identify-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The unique ID of the contact to identify. |
| `email` | string | yes | Email address for the contact. |
| `identifiedThrough` | string | no | Source from where the email is acquired. Default: `api`. |

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

Through the native Salespanel API, this operation is `POST /contacts/:contact_id/identify/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-contact.md) for the provider-specific parameters and requirements.

