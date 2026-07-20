# Blaze AI: List Workspace Properties

Retrieves workspace properties from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspace-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspace-properties?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace_id=994619" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspace_id": "994619"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspace-properties?${params}`, {
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
| `workspace_id` | number | yes | Default: `994619`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "defaultForArticles": true,
          "id": 1,
          "meta": {
            "dateFormat": "string",
            "numberFormat": "string"
          },
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].defaultForArticles` | boolean |  |
| `data[].id` | number |  |
| `data[].meta.dateFormat` | string |  |
| `data[].meta.numberFormat` | string |  |
| `data[].name` | string |  |
| `data[].type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/properties` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-properties.md) for the provider-specific parameters and requirements.

