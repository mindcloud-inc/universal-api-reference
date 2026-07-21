# BlazeMeter: Delete Workspace Tag

Deletes a workspace tag from BlazeMeter.

```
DELETE https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/delete-workspace-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlazeMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/delete-workspace-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/delete-workspace-tag?${params}`, {
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
| `tagId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider response payload. |
| `id` | string | Optional response identifier. |
| `message` | string | Optional response message. |
| `meta` | object | Execution metadata including request/response details. |
| `success` | boolean | Whether the action run succeeded. |

## Native endpoint

Through the native BlazeMeter API, this operation is `DELETE /workspaces/:workspaceId/tags/:tagId` (base URL `https://a.blazemeter.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workspace-tag.md) for the provider-specific parameters and requirements.

