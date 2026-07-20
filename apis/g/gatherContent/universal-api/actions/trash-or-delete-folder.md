# GatherContent: Trash Or Delete Folder

Trashes or permanently deletes a folder in GatherContent.

```
DELETE https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/trash-or-delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/trash-or-delete-folder?connectionId=$CONNECTION_ID&folder_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/trash-or-delete-folder?${params}`, {
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
| `folder_uuid` | string | yes | Folder UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `DELETE /folders/:folder_uuid` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trash-or-delete-folder.md) for the provider-specific parameters and requirements.

