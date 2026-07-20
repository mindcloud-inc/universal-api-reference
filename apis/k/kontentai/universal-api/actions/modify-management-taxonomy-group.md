# Kontent.ai: Modify management taxonomy group

Modifies a taxonomy group in Kontent.ai.

```
PUT https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-taxonomy-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-taxonomy-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taxonomyGroupIdentifier": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-taxonomy-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taxonomyGroupIdentifier": "string",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxonomyGroupIdentifier` | string | yes | Kontent.ai taxonomy group identifier to modify. |
| `operations[]` | array<object> | yes | JSON Patch operations for modifying a Kontent.ai taxonomy group. |

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

Through the native Kontent.ai API, this operation is `PATCH https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-management-taxonomy-group.md) for the provider-specific parameters and requirements.

