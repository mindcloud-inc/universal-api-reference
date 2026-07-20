# Smoove: List Contact Lists

Retrieves contact lists from Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-lists?${params}`, {
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
| `fields` | string | no |  |
| `includeContactsCount` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "permissions": {
        "allowsUsersToSubscribe": true,
        "allowsUsersToUnsubscribe": true,
        "isPortal": true,
        "isPublic": true
      },
      "publicDescription": "string",
      "publicName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `permissions.allowsUsersToSubscribe` | boolean |  |
| `permissions.allowsUsersToUnsubscribe` | boolean |  |
| `permissions.isPortal` | boolean |  |
| `permissions.isPublic` | boolean |  |
| `publicDescription` | string |  |
| `publicName` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Lists` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

