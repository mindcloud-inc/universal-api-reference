# Blaze AI: Get Import

Retrieves a document import from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-import?connectionId=$CONNECTION_ID&workspace_id=994619&id=619" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "994619",
  "id": "619"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-import?${params}`, {
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
| `id` | number | yes | Default: `619`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "doc": {
          "id": 1,
          "key": "string",
          "title": "string"
        },
        "id": 1,
        "status": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.doc.id` | number |  |
| `data.doc.key` | string |  |
| `data.doc.title` | string |  |
| `data.id` | number |  |
| `data.status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/imports/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import.md) for the provider-specific parameters and requirements.

