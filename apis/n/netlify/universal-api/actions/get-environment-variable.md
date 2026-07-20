# Netlify: Get Environment Variable



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-environment-variable?connectionId=$CONNECTION_ID&accountId=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-environment-variable?${params}`, {
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
| `key` | string | yes | The environment variable key (case-sensitive). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | no | Return the environment variable for a specific site. |

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

Through the native Netlify API, this operation is `GET /accounts/:account_id/env/:key` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment-variable.md) for the provider-specific parameters and requirements.

