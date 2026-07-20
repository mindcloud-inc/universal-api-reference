# Buildkite: Get Organization Member

Retrieves an organization member from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-organization-member?connectionId=$CONNECTION_ID&organization=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-organization-member?${params}`, {
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
| `organization` | string | yes | The Buildkite organization slug. |
| `user` | string | yes | The Buildkite user ID or slug for the organization member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "role": "string",
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `role` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `GET /organizations/:organization/members/:user` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-member.md) for the provider-specific parameters and requirements.

