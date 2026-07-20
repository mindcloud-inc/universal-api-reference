# Halo Service Solutions: Get User

Retrieves a user from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | User ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": 1,
      "client_name": "Ava Chen",
      "datecreated": "2026-05-07T12:00:00.000Z",
      "emailaddress": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "name": "Ava Chen",
      "site_id": 1,
      "site_name": "Ava Chen",
      "surname": "Ava Chen",
      "web_access_level": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | number |  |
| `client_name` | string |  |
| `datecreated` | date |  |
| `emailaddress` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `name` | string |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `surname` | string |  |
| `web_access_level` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Users/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

