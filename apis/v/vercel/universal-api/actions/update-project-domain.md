# Vercel: Update Project Domain

Updates an existing project domain in Vercel.

```
PUT https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrName": "prj_1234567890",
  "domain": "mindcloud-vercel-stage3.example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-domain', {
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
| `redirect` | string | no | The redirect target for the project domain Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apexName": "Ava Chen",
      "createdAt": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "redirect": "string",
      "updatedAt": 1,
      "verification": [
        {}
      ],
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apexName` | string | The apex domain name |
| `createdAt` | number | Domain creation timestamp |
| `name` | string | The project domain name |
| `projectId` | string | The owning project identifier |
| `redirect` | string | The redirect target, if configured |
| `updatedAt` | number | Domain update timestamp |
| `verification` | array<object> | Domain verification requirements |
| `verified` | boolean | Whether the domain is verified |

## Native endpoint

Through the native Vercel API, this operation is `PATCH /v9/projects/:idOrName/domains/:domain` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-domain.md) for the provider-specific parameters and requirements.

