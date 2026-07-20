# Uku: Get Client Group

Retrieves a client group from Uku.

```
GET https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client-group?connectionId=$CONNECTION_ID&clientGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client-group?${params}`, {
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
| `clientGroupId` | string | yes | Uku client group ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "initials": "string",
      "members_count": 1,
      "name": "Ava Chen",
      "role": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `members_count` | number |  |
| `name` | string |  |
| `role` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uku API, this operation is `GET /client_groups/:clientGroupId` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-group.md) for the provider-specific parameters and requirements.

