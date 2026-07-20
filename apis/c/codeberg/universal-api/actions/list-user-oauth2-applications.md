# Codeberg: List User OAuth2 Applications



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-oauth2-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-oauth2-applications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-oauth2-applications?${params}`, {
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
      "client_id": "string",
      "client_secret": "string",
      "confidential_client": true,
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "redirect_uris": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string |  |
| `client_secret` | string |  |
| `confidential_client` | boolean |  |
| `created` | date |  |
| `id` | number |  |
| `name` | string |  |
| `redirect_uris` | array<string> |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/applications/oauth2` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-oauth2-applications.md) for the provider-specific parameters and requirements.

