# Smoove: Create List

Creates a new contact list in Smoove.

```
POST https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `publicName` | string | no |  |
| `description` | string | no |  |
| `publicDescription` | string | no |  |
| `permissions.isPublic` | boolean | no |  |
| `permissions.allowsUsersToSubscribe` | boolean | no |  |
| `permissions.allowsUsersToUnsubscribe` | boolean | no |  |
| `permissions.isPortal` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "publicName": "Ava Chen",
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
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `permissions.allowsUsersToSubscribe` | boolean |  |
| `permissions.allowsUsersToUnsubscribe` | boolean |  |
| `permissions.isPortal` | boolean |  |
| `permissions.isPublic` | boolean |  |
| `publicDescription` | string |  |
| `publicName` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Smoove API, this operation is `POST /v1/Lists` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

