# Formstack Documents: Create Data Route

Creates a new data route in Formstack Documents.

```
POST https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folder` | string | no | Folder name to save the data route in |
| `name` | string | yes | Name of the data route |
| `outputName` | string | no | Custom filename for the combined PDF output |
| `rules[].combine` | string | no | Whether to include each rule in the combined PDF |
| `rules[].documentId` | string | no | Document ID for each data route rule |
| `rules[].file` | string | no | Remote file URL or merge field for each rule |
| `rules[].loopField` | string | no | Array field used to repeat a rule |
| `rules[].sort` | string | no | Sort order for each rule |

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

Through the native Formstack Documents API, this operation is `POST /routes` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-route.md) for the provider-specific parameters and requirements.

