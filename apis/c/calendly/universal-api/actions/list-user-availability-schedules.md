# Calendly: List User Availability Schedules

Retrieves user availability schedules from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-availability-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-availability-schedules?connectionId=$CONNECTION_ID&user=https%3A%2F%2Fapi.calendly.com%2Fusers%2F264e5a40-147f-45f9-a96c-a6f2f0a91dff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-user-availability-schedules?${params}`, {
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
| `user` | list | yes | User URI filter. One of: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. Default: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | User availability schedule records. |

## Native endpoint

Through the native Calendly API, this operation is `GET /user_availability_schedules` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-availability-schedules.md) for the provider-specific parameters and requirements.

