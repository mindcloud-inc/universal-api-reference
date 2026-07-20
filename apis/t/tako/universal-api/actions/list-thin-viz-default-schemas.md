# Tako: List Thin-Viz Default Schemas

Retrieves Thin-Viz default schemas from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-thin-viz-default-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-thin-viz-default-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-thin-viz-default-schemas?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
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
| `components` | array<string> | List of component types in this schema |
| `description` | string | Schema description |
| `name` | string | Schema name (unique identifier) |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/thin_viz/default_schema/` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-thin-viz-default-schemas.md) for the provider-specific parameters and requirements.

