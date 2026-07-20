# Joonto: Get Avatar Image By User Email



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-avatar-image-by-user-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-avatar-image-by-user-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-avatar-image-by-user-email?${params}`, {
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
| `email` | string | no |  |
| `size` | string | no | Default: `thumbnail`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Joonto API returns.

## Native endpoint

Through the native Joonto API, this operation is `GET /api/Images/GetByUserEmail` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-image-by-user-email.md) for the provider-specific parameters and requirements.

