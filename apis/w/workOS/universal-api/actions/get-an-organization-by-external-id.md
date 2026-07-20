# WorkOS: Get an Organization by External ID

Retrieves an organization by external ID from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-by-external-id?connectionId=$CONNECTION_ID&external_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "external_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-organization-by-external-id?${params}`, {
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
| `external_id` | string | yes | The external ID of the Organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_profiles_outside_organization": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "domains": [
        {}
      ],
      "external_id": "string",
      "id": "string",
      "message": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "stripe_customer_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_profiles_outside_organization` | boolean | Whether the Organization allows profiles outside of its managed domains. |
| `created_at` | date | An ISO 8601 timestamp. |
| `domains` | array<object> | List of Organization Domains. |
| `external_id` | string | The external ID of the Organization. |
| `id` | string | Unique identifier of the Organization. |
| `message` | string | WorkOS response field message. |
| `metadata` | object | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `name` | string | A descriptive name for the Organization. This field does not need to be unique. |
| `object` | string | Distinguishes the Organization object. |
| `stripe_customer_id` | string | The Stripe customer ID of the Organization. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /organizations/external_id/{external_id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-organization-by-external-id.md) for the provider-specific parameters and requirements.

