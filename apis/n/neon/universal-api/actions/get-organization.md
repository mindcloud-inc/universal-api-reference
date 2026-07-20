# Neon: Retrieve organization details

Retrieves organization details from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization?connectionId=$CONNECTION_ID&org_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_hipaa_projects": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "handle": "string",
      "id": "string",
      "managed_by": "string",
      "name": "Ava Chen",
      "plan": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_hipaa_projects` | boolean |  |
| `created_at` | date |  |
| `handle` | string |  |
| `id` | string |  |
| `managed_by` | string |  |
| `name` | string |  |
| `plan` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Neon API, this operation is `GET /organizations/:org_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

