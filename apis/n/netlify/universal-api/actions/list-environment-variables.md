# Netlify: List Environment Variables



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-environment-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-environment-variables?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-environment-variables?${params}`, {
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
| `accountId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | no | Only return environment variables set on this site. |
| `contextName` | list<string> | no | Filter by deploy context. One of: `all`, `branch-deploy`, `deploy-preview`, `dev`, `dev-server`, `production`. |
| `scope` | list<string> | no | Filter by scope. One of: `builds`, `functions`, `post-processing`, `runtime`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSecret": true,
      "key": "string",
      "scopes": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSecret` | boolean | Whether the value is secret |
| `key` | string | Environment variable key |
| `scopes` | array<string> | Scopes where the variable is available |
| `updatedAt` | date | Last update timestamp |
| `values` | array<object> | Environment variable values by context |

## Native endpoint

Through the native Netlify API, this operation is `GET /accounts/:account_id/env` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environment-variables.md) for the provider-specific parameters and requirements.

