# Formstack Documents: Update Data Route

Updates an existing data route in Formstack Documents.

```
PUT https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-data-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-data-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-data-route', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folder` | string | no | Updated folder name |
| `id` | string | yes | ID of the data route to update |
| `name` | string | no | Updated data route name |
| `outputName` | string | no | Updated custom filename for combined output |
| `rules[].combine` | string | no | Whether to include each rule in the combined PDF |
| `rules[].combineDocx` | string | no | Whether to include each rule in the combined DOCX |
| `rules[].documentId` | string | no | Updated document ID for each rule |
| `rules[].file` | string | no | Updated remote file URL or merge field for each rule |
| `rules[].id` | string | no | Existing rule ID when updating a data route |
| `rules[].loopField` | string | no | Array field used to repeat a rule |
| `rules[].sort` | string | no | Updated sort order for each rule |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "rules": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `rules` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `PUT /routes/:id` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-route.md) for the provider-specific parameters and requirements.

