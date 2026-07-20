# Crossmint: Revoke Credential

Revokes a credential in Crossmint.

```
DELETE https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/revoke-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/revoke-credential?connectionId=$CONNECTION_ID&id=urn%3Auuid%3Aff8be7d6-adc3-4524-b8ee-737564d31357" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "urn:uuid:ff8be7d6-adc3-4524-b8ee-737564d31357"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/revoke-credential?${params}`, {
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
| `id` | string | yes | Credential identifier in `urn:uuid:<UUID>` format. Example: `urn:uuid:ff8be7d6-adc3-4524-b8ee-737564d31357`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actionId": "string",
      "completedAt": "string",
      "data": {},
      "resource": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Crossmint action type. |
| `actionId` | string | Credential revoke action identifier. |
| `completedAt` | string | When the revoke completed, when available. |
| `data` | object | Credential revoke payload details. |
| `resource` | string | Action resource URL. |
| `startedAt` | string | When the revoke started. |
| `status` | string | Current processing status. |

## Native endpoint

Through the native Crossmint API, this operation is `DELETE /v1-alpha1/credentials/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-credential.md) for the provider-specific parameters and requirements.

