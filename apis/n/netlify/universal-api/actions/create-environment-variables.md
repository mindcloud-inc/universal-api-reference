# Netlify: Create Environment Variables



```
POST https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-environment-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-environment-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-environment-variables', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `[]` | array<object> | no | The environment variables to create. |
| `[].key` | string | no |  |
| `[].values[]` | array<object> | no |  |
| `[].values[].value` | string | no |  |
| `[].values[].context` | list<string> | no | One of: `all`, `branch-deploy`, `deploy-preview`, `dev`, `dev-server`, `production`. |
| `[].isSecret` | boolean | no | Secret values are only readable by code running on Netlify's systems. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | no | Create the environment variables on this site instead of at the account level. |
| `[].scopes` | list<string> | no | The scopes that this environment variable is set to. One of: `builds`, `functions`, `post-processing`, `runtime`. |
| `[].values[].id` | string | no |  |
| `[].values[].contextParameter` | string | no |  |

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

Through the native Netlify API, this operation is `POST /accounts/:account_id/env` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-environment-variables.md) for the provider-specific parameters and requirements.

