# Zendesk: Get Current User

Retrieves the current user from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-current-user?${params}`, {
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
      "authenticityToken": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "ianaTimeZone": "string",
      "id": 1,
      "locale": "string",
      "localeId": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "role": "string",
      "timeZone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticityToken` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `ianaTimeZone` | string |  |
| `id` | number |  |
| `locale` | string |  |
| `localeId` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `role` | string |  |
| `timeZone` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Zendesk API, this operation is `GET /users/me.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

