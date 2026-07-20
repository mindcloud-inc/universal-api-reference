# Vercel: List Project Domains

Retrieves all project domains from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-domains?connectionId=$CONNECTION_ID&idOrName=prj_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-domains?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains` | array<object> | The project domains returned by the query |
| `pagination` | object | Pagination metadata for the domain list |

## Native endpoint

Through the native Vercel API, this operation is `GET /v9/projects/:idOrName/domains` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-domains.md) for the provider-specific parameters and requirements.

