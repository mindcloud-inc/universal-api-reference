# Vercel: Assign Alias

Assigns an alias to a Vercel deployment.

```
POST https://connect.mindcloud.co/v1/universal/vercel/latest/actions/assign-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/assign-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alias": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/assign-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alias": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | yes | The alias hostname to assign to the deployment. |
| `id` | string | yes | The deployment ID to assign the alias to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `created` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `POST /v2/deployments/:id/aliases` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-alias.md) for the provider-specific parameters and requirements.

