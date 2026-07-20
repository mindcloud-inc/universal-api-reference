# Vercel: Verify Project Domain

Verifies a project domain in Vercel.

```
PUT https://connect.mindcloud.co/v1/universal/vercel/latest/actions/verify-project-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/verify-project-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrName": "prj_1234567890",
  "domain": "mindcloud-vercel-stage3.example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/verify-project-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idOrName": "prj_1234567890",
    "domain": "mindcloud-vercel-stage3.example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |
| `domain` | string | yes | The project domain name Example: `mindcloud-vercel-stage3.example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `POST /v9/projects/:idOrName/domains/:domain/verify` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-project-domain.md) for the provider-specific parameters and requirements.

