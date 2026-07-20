# Tako: Get Thin-Viz Default Schema

Retrieves a Thin-Viz default schema from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-thin-viz-default-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-thin-viz-default-schema?connectionId=$CONNECTION_ID&schemaName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-thin-viz-default-schema?${params}`, {
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
| `schemaName` | string | yes | Name of the default schema to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "component_templates": [
        {}
      ],
      "components": [
        "string"
      ],
      "description": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `component_templates` | array<object> | Template information for each component type |
| `components` | array<string> | List of component types |
| `description` | string | Schema description |
| `name` | string | Schema name (unique identifier) |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/thin_viz/default_schema/{schema_name}/` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thin-viz-default-schema.md) for the provider-specific parameters and requirements.

