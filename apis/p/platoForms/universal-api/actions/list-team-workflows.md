# PlatoForms: List Team Workflows

Retrieves team workflow details from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-team-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-team-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-team-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "shared_url": "https://example.com",
      "status": "string",
      "steps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `shared_url` | string |  |
| `status` | string |  |
| `steps` | object |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /workflows/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-workflows.md) for the provider-specific parameters and requirements.

