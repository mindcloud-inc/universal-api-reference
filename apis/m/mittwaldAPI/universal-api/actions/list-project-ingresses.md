# mittwald: List Project Ingresses

Retrieves project ingresses from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-ingresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-ingresses?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-ingresses?${params}`, {
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
| `projectId` | string | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hostname": "Ava Chen",
      "id": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hostname` | string |  |
| `id` | string |  |
| `target` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/projects/:projectId/ingresses` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-ingresses.md) for the provider-specific parameters and requirements.

