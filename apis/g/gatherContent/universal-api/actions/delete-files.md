# GatherContent: Delete Files

Deletes files from a GatherContent project.

```
DELETE https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/delete-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/delete-files?connectionId=$CONNECTION_ID&file_ids=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_ids": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/delete-files?${params}`, {
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
| `file_ids` | string | yes | File IDs to delete. |
| `project_id` | string | yes | Project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "file_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `file_ids` | array<string> |  |

## Native endpoint

Through the native GatherContent API, this operation is `DELETE /projects/:project_id/files` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files.md) for the provider-specific parameters and requirements.

