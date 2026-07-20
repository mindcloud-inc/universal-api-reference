# Quire: Get Current User

Retrieves the current user from Quire.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user?${params}`, {
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
      "description": "string",
      "descriptionHtml": "string",
      "descriptionText": "string",
      "email": "ava@example.com",
      "iconColor": "string",
      "id": "string",
      "image": "string",
      "locale": "string",
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "nameText": "Ava Chen",
      "oid": "string",
      "timeZone": {},
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `descriptionText` | string |  |
| `email` | string |  |
| `iconColor` | string |  |
| `id` | string |  |
| `image` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `nameHtml` | string |  |
| `nameText` | string |  |
| `oid` | string |  |
| `timeZone` | object |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Quire API, this operation is `GET user/id/me` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

