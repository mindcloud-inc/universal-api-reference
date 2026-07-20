# Castor EDC: Get User

Retrieves a user from Castor EDC by ID.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-user?connectionId=$CONNECTION_ID&user_id=6542DEB5-3222-4436-A79D-A6F95BECC5A4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "6542DEB5-3222-4436-A79D-A6F95BECC5A4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-user?${params}`, {
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
| `user_id` | string | yes | The ID of the user to retrieve Example: `6542DEB5-3222-4436-A79D-A6F95BECC5A4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "email_address": "ava@example.com",
      "entity_id": "string",
      "full_name": "Ava Chen",
      "id": "string",
      "last_login": "string",
      "name_first": "Ava Chen",
      "name_last": "Ava Chen",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string |  |
| `email_address` | string |  |
| `entity_id` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `last_login` | string |  |
| `name_first` | string |  |
| `name_last` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /user/:user_id` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

