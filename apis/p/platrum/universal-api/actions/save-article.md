# Platrum: Save article

Creates or updates a knowledge article in Platrum.

```
POST https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content_blocks[]": [
    {}
  ],
  "space_ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content_blocks[]": [{}],
    "space_ids[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access_comment[]` | array<object> | no | Comment access rules. |
| `access_edit[]` | array<object> | no | Edit access rules. |
| `access[]` | array<object> | no | View access rules. |
| `content_blocks[]` | array<object> | yes | Article content blocks. |
| `id` | number | no | Article ID for updates. |
| `parent_ids[]` | array<number> | no | Parent article IDs. |
| `slug` | string | no | Article slug. |
| `space_ids[]` | array<number> | yes | Target space IDs. |
| `title` | string | no | Article title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /wiki/api/article/save` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-article.md) for the provider-specific parameters and requirements.

