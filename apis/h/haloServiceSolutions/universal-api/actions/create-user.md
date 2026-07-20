# Halo Service Solutions: Create User

Creates a new user in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "site_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "site_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `site_id` | number | yes |  |
| `firstname` | string | no |  |
| `surname` | string | no |  |
| `emailaddress` | string | no |  |

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

Through the native Halo Service Solutions API, this operation is `POST /Users` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

