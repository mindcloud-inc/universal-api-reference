# Kontent.ai: Retrieve taxonomy group

Retrieves a taxonomy group from Kontent.ai.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-taxonomy-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-taxonomy-group?connectionId=$CONNECTION_ID&environmentId=string&taxonomyGroupCodename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "string",
  "taxonomyGroupCodename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-taxonomy-group?${params}`, {
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
| `environmentId` | string | yes | Kontent.ai project environment identifier. |
| `taxonomyGroupCodename` | string | yes | Taxonomy group codename. |

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

Through the native Kontent.ai API, this operation is `GET /:environment_id/taxonomies/:taxonomy_group_codename` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-taxonomy-group.md) for the provider-specific parameters and requirements.

