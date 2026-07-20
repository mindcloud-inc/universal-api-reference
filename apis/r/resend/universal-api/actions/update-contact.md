# Resend: Update Contact

Updates an existing contact in Resend.

```
PUT https://connect.mindcloud.co/v1/universal/resend/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/resend/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "cnt_01J1K4M6Z8Q3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "cnt_01J1K4M6Z8Q3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | list<string> | no | Example: `ava.thompson@example.com`. |
| `firstName` | string | no | Example: `Ava`. |
| `id` | string<string> | yes | Example: `cnt_01J1K4M6Z8Q3`. |
| `lastName` | string | no | Example: `Thompson`. |
| `unsubscribed` | boolean | no | If set to true, the contact will be unsubscribed from all Broadcasts. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | no | A map of custom property key-value pairs to update on the contact. |

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

Through the native Resend API, this operation is `PATCH /contacts/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

