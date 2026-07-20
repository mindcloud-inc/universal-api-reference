# Umbler Talk: Get Contact

Retrieves a contact from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The contact ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "channelIds": [
        "string"
      ],
      "contactType": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "isBlocked": true,
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "phoneNumber": "string",
      "profilePictureUrl": "https://example.com",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `channelIds` | array<string> |  |
| `contactType` | string |  |
| `createdAtUTC` | date |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `phoneNumber` | string |  |
| `profilePictureUrl` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/contacts/[:id]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

