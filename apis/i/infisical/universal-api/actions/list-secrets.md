# Infisical: List Secrets

Retrieves secrets from a project environment in Infisical.

```
GET https://connect.mindcloud.co/v1/universal/infisical/latest/actions/list-secrets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infisical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/list-secrets?connectionId=$CONNECTION_ID&projectId=string&environment=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "environment": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infisical/latest/actions/list-secrets?${params}`, {
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
| `projectId` | string | yes | The Infisical project ID to list secrets from. |
| `environment` | string | yes | The environment slug to list secrets from. |
| `secretPath` | string | no | The secret path to list secrets from. Defaults to /. Default: `/`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infisical API returns.

## Native endpoint

Through the native Infisical API, this operation is `GET /api/v4/secrets` (base URL `https://app.infisical.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-secrets.md) for the provider-specific parameters and requirements.

