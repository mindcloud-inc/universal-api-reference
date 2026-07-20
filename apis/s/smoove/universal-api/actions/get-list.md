# Smoove: Get List

Retrieves a contact list from Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-list?${params}`, {
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
| `id` | string | yes |  |
| `fields` | string | no |  |

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

Through the native Smoove API, this operation is `GET /v1/Lists/:id` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

