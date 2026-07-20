# Softr: Delete User



```
DELETE https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-user?connectionId=$CONNECTION_ID&email=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-user?${params}`, {
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
| `email` | string | yes | Email address of the Softr user to delete. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |

## Native endpoint

Through the native Softr API, this operation is `DELETE https://studio-api.softr.io/v1/api/users/:email` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

