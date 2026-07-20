# Vercel: List Deployment Files

Retrieves all deployment files from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-deployment-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-deployment-files?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-deployment-files?${params}`, {
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
| `id` | string | yes | The unique identifier of the deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "mode": 1,
      "name": "Ava Chen",
      "type": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `mode` | number |  |
| `name` | string |  |
| `type` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v6/deployments/:id/files` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployment-files.md) for the provider-specific parameters and requirements.

