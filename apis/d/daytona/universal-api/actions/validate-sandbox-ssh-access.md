# Daytona: Validate Sandbox SSH Access

Validates sandbox SSH access in Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/validate-sandbox-ssh-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/validate-sandbox-ssh-access?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/validate-sandbox-ssh-access?${params}`, {
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
| `token` | string | yes | SSH access token to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sandboxId": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sandboxId` | string | ID of the sandbox this SSH access is for. |
| `valid` | boolean | Whether the SSH access token is valid. |

## Native endpoint

Through the native Daytona API, this operation is `GET /sandbox/ssh-access/validate` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-sandbox-ssh-access.md) for the provider-specific parameters and requirements.

