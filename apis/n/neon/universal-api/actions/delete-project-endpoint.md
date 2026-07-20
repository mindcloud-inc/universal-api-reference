# Neon: Delete compute endpoint

Deletes a compute endpoint from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-endpoint?connectionId=$CONNECTION_ID&project_id=string&endpoint_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "endpoint_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-endpoint?${params}`, {
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
| `endpoint_id` | string | yes | Neon API parameter endpoint_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoint": {},
      "operations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoint` | object |  |
| `operations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/endpoints/:endpoint_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-endpoint.md) for the provider-specific parameters and requirements.

