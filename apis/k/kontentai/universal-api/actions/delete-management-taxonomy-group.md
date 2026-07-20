# Kontent.ai: Delete management taxonomy group

Deletes a taxonomy group from Kontent.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-taxonomy-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-taxonomy-group?connectionId=$CONNECTION_ID&taxonomyGroupIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxonomyGroupIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-taxonomy-group?${params}`, {
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
| `taxonomyGroupIdentifier` | string | yes | Kontent.ai taxonomy group identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete request completed successfully. |

## Native endpoint

Through the native Kontent.ai API, this operation is `DELETE https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-management-taxonomy-group.md) for the provider-specific parameters and requirements.

