# Neon: Retrieve connection URI

Retrieves a connection URI from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-connection-uri
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-connection-uri?connectionId=$CONNECTION_ID&project_id=string&database_name=Ava%20Chen&role_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "database_name": "Ava Chen",
  "role_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-connection-uri?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `database_name` | string | yes | Neon API parameter database_name |
| `role_name` | string | yes | Neon API parameter role_name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch_id` | string | no | Neon API parameter branch_id |
| `endpoint_id` | string | no | Neon API parameter endpoint_id |
| `pooled` | boolean | no | Neon API parameter pooled |

## Response

```json
{
  "success": true,
  "data": [
    {
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `uri` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/connection_uri` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-uri.md) for the provider-specific parameters and requirements.

