# Conexteo: Create Contact List

Creates a contact list in Conexteo.

```
POST https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-contact-list', {
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
| `name` | string | no | Name of the contact list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "rcsCapabilityStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts_count` | number | Number of contacts in the list. |
| `id` | number | Contact-list identifier. |
| `name` | string | Contact-list name. |
| `rcsCapabilityStatus` | string | Provider RCS capability status for the list. |

## Native endpoint

Through the native Conexteo API, this operation is `POST /contactlists` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-list.md) for the provider-specific parameters and requirements.

