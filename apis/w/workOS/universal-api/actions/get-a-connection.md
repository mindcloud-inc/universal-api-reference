# WorkOS: Get a Connection

Retrieves a connection from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-connection?connectionId=$CONNECTION_ID&id=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-connection?${params}`, {
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
| `id` | string | yes | Unique identifier for the Connection. |
| `id` | string | yes | Unique identifier for the Connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connection_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "domains": [
        {}
      ],
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "object": "string",
      "options": {},
      "organization_id": "string",
      "state": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection_type` | string | The type of the SSO Connection used to authenticate the user. The Connection type may be used to dynamically generate authorization URLs. |
| `created_at` | date | An ISO 8601 timestamp. |
| `domains` | array<object> | List of Organization Domains. |
| `id` | string | Unique identifier for the Connection. |
| `message` | string | WorkOS response field message. |
| `name` | string | A human-readable name for the Connection. This will most commonly be the organization's name. |
| `object` | string | Distinguishes the Connection object. |
| `options` | object | Configuration options for SAML connections. Only present for SAML connection types. |
| `organization_id` | string | Unique identifier for the Organization in which the Connection resides. |
| `state` | string | Indicates whether a Connection is able to authenticate users. |
| `status` | string | Deprecated. Use `state` instead. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /connections/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-connection.md) for the provider-specific parameters and requirements.

