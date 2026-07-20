# Devin: Create Secret

Creates a new secret in Devin.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "orgId": "string",
  "type": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "orgId": "string",
    "type": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isSensitive` | boolean | no | Whether the secret is sensitive. |
| `key` | string | yes | Secret key/name. |
| `note` | string | no | Optional note for the secret. |
| `orgId` | string | yes | Devin organization ID. |
| `type` | string | yes | Secret type: cookie, key-value, or totp. |
| `value` | string | yes | Secret value. |

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
| `secret_id` | string | Secret ID. |
| `secret_type` | string | Secret type. |
| `updated_at` | number | Update timestamp. |
| `updated_by` | string | Updater identifier. |

## Native endpoint

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/secrets` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-secret.md) for the provider-specific parameters and requirements.

