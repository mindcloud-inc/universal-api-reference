# WEEEK: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEEEK `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The WEEEK contact ID from the contacts API. |
| `firstName` | string | yes | The contact first name. WEEEK required this field during PATCH validation. |
| `lastName` | string | no | The contact last name. |
| `middleName` | string | no | The contact middle name. |
| `organizations[]` | array<string> | no | Optional WEEEK organization IDs to attach to the contact. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | The updated WEEEK contact. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native WEEEK API, this operation is `PATCH /crm/contacts/:contactId` (base URL `https://api.weeek.net/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

