# Heyy: Add Contact Attribute

Adds an attribute to a contact in Heyy.

```
PUT https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-contact-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-contact-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "externalId": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-contact-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "externalId": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Heyy contact ID. |
| `externalId` | string | yes | The contact attribute external ID. |
| `value` | string | yes | The attribute value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isSubscribed": true,
      "labels": [
        {}
      ],
      "lastName": "Chen",
      "phoneNumber": "string",
      "tenantId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isSubscribed` | boolean |  |
| `labels` | array<object> |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `tenantId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /contacts/:contactId/attributes` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-attribute.md) for the provider-specific parameters and requirements.

