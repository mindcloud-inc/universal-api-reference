# Moco: List Assigned Projects



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-assigned-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-assigned-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-assigned-projects?${params}`, {
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
| `active` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billable": true,
      "id": 1,
      "identifier": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billable` | boolean |  |
| `id` | number |  |
| `identifier` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /projects/assigned` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assigned-projects.md) for the provider-specific parameters and requirements.

