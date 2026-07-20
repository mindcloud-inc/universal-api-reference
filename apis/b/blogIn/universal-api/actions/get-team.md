# BlogIn: Get Team

Retrieves a specific team from BlogIn.

```
GET https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/get-team?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/get-team?${params}`, {
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
| `id` | number | yes | The ID of the team to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "id": 1,
      "name": "Ava Chen",
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `position` | number |  |

## Native endpoint

Through the native BlogIn API, this operation is `GET /teams/:id` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

