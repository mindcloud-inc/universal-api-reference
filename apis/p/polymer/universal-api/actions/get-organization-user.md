# Polymer: Get Organization User

Retrieves an organization user from Polymer.

```
GET https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-organization-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polymer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-organization-user?connectionId=$CONNECTION_ID&organization_user_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization_user_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-organization-user?${params}`, {
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
| `organization_user_id` | number | yes | Numeric Polymer organization user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Polymer API returns.

## Native endpoint

Through the native Polymer API, this operation is `GET /organization_users/:organization_user_id` (base URL `https://api.polymer.co/v1/hire`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-user.md) for the provider-specific parameters and requirements.

