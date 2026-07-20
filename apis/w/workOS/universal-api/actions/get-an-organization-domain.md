# WorkOS: Get an Organization Domain

Retrieves an organization domain from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-domain?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-domain?${params}`, {
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
| `id` | string | yes | Unique identifier of the organization domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "message": "string",
      "object": "string",
      "organization_id": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verification_prefix": "string",
      "verification_strategy": "string",
      "verification_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `domain` | string | Domain for the organization domain. |
| `id` | string | Unique identifier of the organization domain. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the organization domain object. |
| `organization_id` | string | ID of the parent Organization. |
| `state` | string | Verification state of the domain. |
| `updated_at` | date | An ISO 8601 timestamp. |
| `verification_prefix` | string | The prefix used in DNS verification. |
| `verification_strategy` | string | Strategy used to verify the domain. |
| `verification_token` | string | Validation token to be used in DNS TXT record. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /organization_domains/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-organization-domain.md) for the provider-specific parameters and requirements.

