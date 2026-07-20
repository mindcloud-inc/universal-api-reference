# WorkOS: Update an Organization

Updates an organization in your WorkOS environment.

```
PUT https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-an-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-an-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-an-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the Organization. |
| `name` | string | no | The name of the organization. |
| `allow_profiles_outside_organization` | boolean | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | list<string> | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | list<object> | no | The domains associated with the organization, including verification state. |
| `stripe_customer_id` | string | no | The Stripe customer ID associated with the organization. |
| `metadata` | object | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | string | no | An external identifier for the Organization. |
| `id` | string | yes | Unique identifier of the Organization. |
| `name` | string | no | The name of the organization. |
| `allow_profiles_outside_organization` | boolean | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | list<string> | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | list<object> | no | The domains associated with the organization, including verification state. |
| `stripe_customer_id` | string | no | The Stripe customer ID associated with the organization. |
| `metadata` | object | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | string | no | An external identifier for the Organization. |

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

Through the native WorkOS API, this operation is `PUT /organizations/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-an-organization.md) for the provider-specific parameters and requirements.

