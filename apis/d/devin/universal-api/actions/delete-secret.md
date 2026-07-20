# Devin: Delete Secret

Deletes an existing secret from Devin.

```
DELETE https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-secret?connectionId=$CONNECTION_ID&orgId=string&secretId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "secretId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/delete-secret?${params}`, {
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
| `orgId` | string | yes | Devin organization ID. |
| `secretId` | string | yes | Secret ID prefixed with secret-. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_type": "string",
      "created_at": 1,
      "created_by": "string",
      "is_sensitive": true,
      "key": "string",
      "note": "string",
      "secret_id": "string",
      "secret_type": "string",
      "updated_at": 1,
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_type` | string | Access scope. |
| `created_at` | number | Creation timestamp. |
| `created_by` | string | Creator identifier. |
| `is_sensitive` | boolean | Whether the secret is sensitive. |
| `key` | string | Secret key. |
| `note` | string | Secret note. |
| `secret_id` | string | Deleted secret ID. |
| `secret_type` | string | Secret type. |
| `updated_at` | number | Update timestamp. |
| `updated_by` | string | Updater identifier. |

## Native endpoint

Through the native Devin API, this operation is `DELETE /v3/organizations/:org_id/secrets/:secret_id` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-secret.md) for the provider-specific parameters and requirements.

