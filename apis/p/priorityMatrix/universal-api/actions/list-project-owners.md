# Priority Matrix: List Project Owners

Retrieves owners for a Priority Matrix project.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-owners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-owners?connectionId=$CONNECTION_ID&idd=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idd": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-owners?${params}`, {
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
| `idd` | number | yes | Project IDD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "resource_uri": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | number |  |
| `resource_uri` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/project/:idd/owners/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-owners.md) for the provider-specific parameters and requirements.

