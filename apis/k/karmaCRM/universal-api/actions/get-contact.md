# Karma CRM: Get Contact

Retrieves a specific contact from Karma CRM.

```
GET https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The ID of the contact to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "background": "string",
      "createdAt": "string",
      "createdById": 1,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "organizationId": 1,
      "position": "string",
      "private": true,
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `background` | string |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `organizationId` | number |  |
| `position` | string |  |
| `private` | boolean |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `GET /api/v3/contacts/:id.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

