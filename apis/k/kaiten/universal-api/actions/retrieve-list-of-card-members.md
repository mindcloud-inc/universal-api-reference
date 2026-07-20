# Kaiten: Retrieve List of Card Members

Retrieves members for a Kaiten card.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-members?connectionId=$CONNECTION_ID&cardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-members?${params}`, {
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
| `cardId` | number | yes | The Kaiten card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": true,
      "avatar_initials_url": "https://example.com",
      "avatar_type": 1,
      "avatar_uploaded_url": "https://example.com",
      "created": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "initials": "string",
      "lng": "string",
      "theme": "string",
      "timezone": "string",
      "type": 1,
      "ui_version": 1,
      "uid": "string",
      "updated": "string",
      "username": "Ava Chen",
      "virtual": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | boolean |  |
| `avatar_initials_url` | string |  |
| `avatar_type` | number |  |
| `avatar_uploaded_url` | string |  |
| `created` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `lng` | string |  |
| `theme` | string |  |
| `timezone` | string |  |
| `type` | number |  |
| `ui_version` | number |  |
| `uid` | string |  |
| `updated` | string |  |
| `username` | string |  |
| `virtual` | boolean |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /cards/:cardId/members` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-list-of-card-members.md) for the provider-specific parameters and requirements.

