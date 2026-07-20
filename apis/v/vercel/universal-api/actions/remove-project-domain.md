# Vercel: Remove Project Domain

Removes a domain from a Vercel project.

```
DELETE https://connect.mindcloud.co/v1/universal/vercel/latest/actions/remove-project-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/remove-project-domain?connectionId=$CONNECTION_ID&idOrName=prj_1234567890&domain=mindcloud-vercel-stage3.example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890",
  "domain": "mindcloud-vercel-stage3.example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/remove-project-domain?${params}`, {
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
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |
| `domain` | string | yes | The project domain name Example: `mindcloud-vercel-stage3.example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `DELETE /v9/projects/:idOrName/domains/:domain` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-domain.md) for the provider-specific parameters and requirements.

