# Blaze AI: List Doc Accesses

Retrieves document accesses from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-doc-accesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-doc-accesses?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace_id=994619&doc_id=4981633" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspace_id": "994619",
  "doc_id": "4981633"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-doc-accesses?${params}`, {
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
| `workspace_id` | number | yes | Blaze workspace ID. Default: `994619`. |
| `doc_id` | number | yes | Blaze document ID. Default: `4981633`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "accessorId": 1,
          "accessorType": "string",
          "docId": 1,
          "id": 1,
          "inherited": true,
          "permission": "string"
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
| `data[].accessorId` | number |  |
| `data[].accessorType` | string |  |
| `data[].docId` | number |  |
| `data[].id` | number |  |
| `data[].inherited` | boolean |  |
| `data[].permission` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/docs/:doc_id/accesses` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-doc-accesses.md) for the provider-specific parameters and requirements.

