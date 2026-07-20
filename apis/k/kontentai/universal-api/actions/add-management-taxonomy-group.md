# Kontent.ai: Add management taxonomy group

Creates a new taxonomy group in Kontent.ai.

```
POST https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-taxonomy-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-taxonomy-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-taxonomy-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | JSON request body for creating a Kontent.ai taxonomy group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "terms": [
        {
          "codename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Taxonomy group codename. |
| `id` | string | Taxonomy group ID. |
| `name` | string | Taxonomy group name. |
| `terms[].codename` | string | Taxonomy term codename. |
| `terms[].id` | string | Taxonomy term ID. |
| `terms[].name` | string | Taxonomy term name. |

## Native endpoint

Through the native Kontent.ai API, this operation is `POST https://manage.kontent.ai/v2/projects/:environment_id/taxonomies` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-management-taxonomy-group.md) for the provider-specific parameters and requirements.

