# Resend: Create Contact

Creates a new contact in Resend.

```
POST https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-contact', {
  method: 'POST',
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
| `email` | string | no | Example: `name@example.com`. |
| `topics[].id` | string | no |  |
| `topics[].subscription` | string | no | Accepted values: `opt_in` or `opt_out`. |
| `firstName` | string | no | Example: `Steve`. |
| `lastName` | string | no | Example: `Wozniak`. |
| `unsubscribed` | boolean | no | Sets the contact's global unsubscribe status. When true, the contact is unsubscribed from all broadcasts. Example: `false`. |
| `segments[]` | array<string> | no | Array of segment IDs to add the contact to. |
| `topics[]` | array<object> | no | Array of topic subscription objects with `id` and `subscription` (`opt_in` or `opt_out`). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | no | Object map of custom contact properties as key/value pairs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Contact identifier. |
| `object` | string | Object type identifier. |

## Native endpoint

Through the native Resend API, this operation is `POST /contacts` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

