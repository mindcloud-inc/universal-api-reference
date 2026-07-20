# Postalytics: Update Suppression List Contact

Updates a contact on a Postalytics suppression list.

```
PUT https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/update-suppression-list-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/update-suppression-list-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/update-suppression-list-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Mailing street address. |
| `city` | string | no | Mailing city. |
| `country` | string | no | Mailing country code. |
| `email` | string | no | Suppressed contact email address. |
| `firstName` | string | no | Suppressed contact first name. |
| `lastName` | string | no | Suppressed contact last name. |
| `listId` | number | yes | Suppression list ID. |
| `state` | string | no | Mailing state or province. |
| `zip` | string | no | Mailing postal code. |
| `contactId` | number | yes | Suppression contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContactDetails": [
        {}
      ],
      "ListDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContactDetails` | array<object> | Updated suppression-list contact records. |
| `ListDetails` | object | Suppression list metadata. |

## Native endpoint

Through the native Postalytics API, this operation is `PUT /api/v1/lists/suppression/contacts/:listId/:contactId` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-suppression-list-contact.md) for the provider-specific parameters and requirements.

