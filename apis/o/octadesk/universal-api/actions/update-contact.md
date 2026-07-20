# Octadesk: Update Contact

Updates an existing contact in Octadesk.

```
PUT https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "0ccc5c56-5948-4182-983b-866a05e6efb3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "0ccc5c56-5948-4182-983b-866a05e6efb3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Customer email. |
| `id` | string | yes | Contact ID from Octadesk. Example: `0ccc5c56-5948-4182-983b-866a05e6efb3`. |
| `name` | string | no | Customer name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        "string"
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "organization": {
        "description": "string",
        "domains": [
          "string"
        ],
        "id": "string",
        "name": "Ava Chen"
      },
      "phoneContacts": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organization.description` | string |  |
| `organization.domains[]` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `phoneContacts` | array |  |

## Native endpoint

Through the native Octadesk API, this operation is `PATCH /contacts/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

