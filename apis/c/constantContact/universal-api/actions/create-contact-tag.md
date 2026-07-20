# Constant Contact: Create Contact Tag

Creates a contact tag in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "VIP Customers"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "VIP Customers"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the tag to create. Example: `VIP Customers`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagSource` | string | no | Tag source type when provided by the API. Example: `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "tagId": "string",
      "tagSource": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `name` | string |  |
| `tagId` | string |  |
| `tagSource` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `POST /contact_tags` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-tag.md) for the provider-specific parameters and requirements.

