# Neon: Revoke organization API key

Revokes a organization API key from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-org-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-org-api-key?connectionId=$CONNECTION_ID&org_id=string&key_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string",
  "key_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-org-api-key?${params}`, {
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
| `org_id` | string | yes | Neon API parameter org_id |
| `key_id` | number | yes | Neon API parameter key_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": 1,
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "last_used_from_addr": "string",
      "name": "Ava Chen",
      "project_id": "string",
      "revoked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `created_by` | string |  |
| `id` | number |  |
| `last_used_at` | date |  |
| `last_used_from_addr` | string |  |
| `name` | string |  |
| `project_id` | string |  |
| `revoked` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /organizations/:org_id/api_keys/:key_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-org-api-key.md) for the provider-specific parameters and requirements.

