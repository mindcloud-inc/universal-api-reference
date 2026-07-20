# Nozbe Personal: Get Team

Retrieves a team from Nozbe Personal by ID.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/get-team?connectionId=$CONNECTION_ID&id=L2TZ05o6wV41fjMe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "L2TZ05o6wV41fjMe"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/get-team?${params}`, {
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
| `id` | string | yes | Team ID. Example: `L2TZ05o6wV41fjMe`. |
| `fields` | string | no | Comma-separated fields to return. Example: `id,name,color,sidebar_position,is_personal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "isPersonal": true,
      "name": "Ava Chen",
      "sidebarPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `isPersonal` | boolean |  |
| `name` | string |  |
| `sidebarPosition` | number |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /teams/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

