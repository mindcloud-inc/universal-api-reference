# Zenkit: Get Users For List

Retrieves users for a Zenkit list.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-list?connectionId=$CONNECTION_ID&listAllId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listAllId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-list?${params}`, {
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
| `listAllId` | string | yes | The list all id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayname": "Ava Chen",
      "emailCount": 1,
      "fullname": "Ava Chen",
      "id": 1,
      "imageLink": "https://example.com",
      "initials": "string",
      "isImagePreferred": true,
      "organizationId": 1,
      "registered_at": "2026-05-07T12:00:00.000Z",
      "roleId": "string",
      "shortId": "string",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayname` | string |  |
| `emailCount` | number |  |
| `fullname` | string |  |
| `id` | number |  |
| `imageLink` | string |  |
| `initials` | string |  |
| `isImagePreferred` | boolean |  |
| `organizationId` | number |  |
| `registered_at` | date |  |
| `roleId` | string |  |
| `shortId` | string |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /lists/:listAllId/users` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users-for-list.md) for the provider-specific parameters and requirements.

