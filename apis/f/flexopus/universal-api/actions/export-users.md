# Flexopus: Export Users

Retrieves a user export from Flexopus.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/export-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/export-users?connectionId=$CONNECTION_ID&format=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "format": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/export-users?${params}`, {
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
| `format` | string | yes | The export file format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flexopus API returns.

## Native endpoint

Through the native Flexopus API, this operation is `GET /users/export` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-users.md) for the provider-specific parameters and requirements.

