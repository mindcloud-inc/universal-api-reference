# Microsoft Power BI: Generate Token



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-generate-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-generate-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-generate-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasets[]` | array<object> | no | A list of datasets |
| `datasourceIdentities[]` | array<object> | no | List of identities to use when connecting to data sources with Single Sign-On (SSO) enabled. |
| `identities[]` | array<object> | no | The list of identities to use for row-level security rules |
| `lifetimeInMinutes` | number | no | The maximum lifetime of the token in minutes, starting from the time it was generated. Can be used to shorten the token's expiration time, but not to extend it. The value must be a positive integer. Zero (0) is equivalent to null, and will set the default expiration time. |
| `reports[]` | array<object> | no | A list of reports |
| `targetWorkspaces[]` | array<object> | no | The list of workspaces that the embed token will allow saving to |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST GenerateToken` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embed-token-generate-token.md) for the provider-specific parameters and requirements.

