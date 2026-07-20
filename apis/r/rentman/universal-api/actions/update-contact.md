# Rentman: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/rentman/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rentman/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric ID of the contact to update. |
| `name` | string | no | Contact name. |
| `type` | string | no | Contact type: private or company. |
| `email_1` | string | no | Primary email address. |
| `phone_1` | string | no | Primary phone number. |
| `mailing_city` | string | no | Mailing city. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "default_person": "string",
      "displayname": "Ava Chen",
      "email_1": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "image": "string",
      "mailing_city": "string",
      "mailing_postalcode": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone_1": "string",
      "surname": "Ava Chen",
      "tags": "string",
      "type": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `country` | string |  |
| `created` | date |  |
| `custom` | object |  |
| `default_person` | string |  |
| `displayname` | string |  |
| `email_1` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `image` | string |  |
| `mailing_city` | string |  |
| `mailing_postalcode` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `phone_1` | string |  |
| `surname` | string |  |
| `tags` | string |  |
| `type` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `PUT /contacts/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

