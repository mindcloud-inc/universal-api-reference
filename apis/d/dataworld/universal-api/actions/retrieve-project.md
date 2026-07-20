# data.world: Retrieve Project

Retrieves a data project from data.world.

```
GET https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-project?connectionId=$CONNECTION_ID&owner=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/retrieve-project?${params}`, {
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
| `owner` | string | yes | User or organization owner of the project. |
| `id` | string | yes | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "owner": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `owner` | string |  |
| `title` | string |  |

## Native endpoint

Through the native data.world API, this operation is `GET /projects/{owner}/{id}` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-project.md) for the provider-specific parameters and requirements.

