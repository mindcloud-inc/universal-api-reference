# Karma CRM: List Contacts

Retrieves a list of contacts from Karma CRM.

```
GET https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-contacts?${params}`, {
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
| `page` | number | no | Page number to retrieve. |
| `assignedUserId` | number | no | Filter contacts by assigned user ID. |
| `contactStatusId` | number | no | Filter contacts by contact status ID. |
| `contactStageId` | number | no | Filter contacts by contact stage ID. |
| `tagList` | string | no | Comma-separated tag list filter, for example eastern,night. |

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
| `position` | string |  |
| `private` | boolean |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `GET /api/v3/contacts.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

