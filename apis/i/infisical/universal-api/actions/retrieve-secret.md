# Infisical: Retrieve Secret

Retrieves a secret from a project environment in Infisical.

```
GET https://connect.mindcloud.co/v1/universal/infisical/latest/actions/retrieve-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infisical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/retrieve-secret?connectionId=$CONNECTION_ID&secretName=Ava%20Chen&projectId=string&environment=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "secretName": "Ava Chen",
  "projectId": "string",
  "environment": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infisical/latest/actions/retrieve-secret?${params}`, {
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
| `secretName` | string | yes |  |
| `projectId` | string | yes |  |
| `environment` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infisical API returns.

## Native endpoint

Through the native Infisical API, this operation is `GET /api/v4/secrets/:secretName` (base URL `https://app.infisical.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-secret.md) for the provider-specific parameters and requirements.

