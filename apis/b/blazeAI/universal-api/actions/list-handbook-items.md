# Blaze AI: List Handbook Items

Retrieves handbook items from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-handbook-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-handbook-items?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace_id=994619&handbook_id=3412870" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspace_id": "994619",
  "handbook_id": "3412870"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-handbook-items?${params}`, {
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
| `handbook_id` | number | yes | Default: `3412870`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "docId": 1,
          "handbookId": 1,
          "id": 1,
          "parentItemId": 1,
          "position": 1,
          "title": "string",
          "type": "string",
          "url": "https://example.com"
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
| `data[].docId` | number |  |
| `data[].handbookId` | number |  |
| `data[].id` | number |  |
| `data[].parentItemId` | number |  |
| `data[].position` | number |  |
| `data[].title` | string |  |
| `data[].type` | string |  |
| `data[].url` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/handbooks/:handbook_id/items` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-handbook-items.md) for the provider-specific parameters and requirements.

