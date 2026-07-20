# Wrike: List Contacts

Finds contacts in Wrike.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "companyName": "Ava Chen",
      "deleted": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "locale": "string",
      "location": "string",
      "me": true,
      "myTeam": true,
      "phone": "string",
      "primaryEmail": "ava@example.com",
      "profiles": [
        {}
      ],
      "timezone": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `companyName` | string |  |
| `deleted` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `locale` | string |  |
| `location` | string |  |
| `me` | boolean |  |
| `myTeam` | boolean |  |
| `phone` | string |  |
| `primaryEmail` | string |  |
| `profiles` | array<object> |  |
| `timezone` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /contacts` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

