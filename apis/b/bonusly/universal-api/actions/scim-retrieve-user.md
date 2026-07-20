# Bonusly: SCIM Retrieve User

Retrieves a SCIM user from Bonusly.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-retrieve-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-retrieve-user?${params}`, {
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
| `id` | string | yes | The SCIM user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "emails": [
        {}
      ],
      "id": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `emails` | array<object> |  |
| `id` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET https://bonus.ly/api/scim11/Users/:id` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scim-retrieve-user.md) for the provider-specific parameters and requirements.

