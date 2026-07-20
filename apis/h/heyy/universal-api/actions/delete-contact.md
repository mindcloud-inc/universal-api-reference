# Heyy: Delete Contact

Deletes an existing contact from Heyy.

```
DELETE https://connect.mindcloud.co/v1/universal/heyy/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/delete-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Heyy contact ID. |

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

Through the native Heyy API, this operation is `DELETE /contacts/:contactId` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

