# Openlayer: Delete Project User Tag

Deletes a project user tag from Openlayer.

```
DELETE https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/delete-project-user-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/delete-project-user-tag?connectionId=$CONNECTION_ID&projectId=2fcd0a42-23a7-44bb-b4fa-4fc3168fe248&tagId=23ad6273-c293-48fc-b44a-f7419da3f866" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "tagId": "23ad6273-c293-48fc-b44a-f7419da3f866"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/delete-project-user-tag?${params}`, {
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
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `tagId` | string | yes | The user tag ID. Default: `23ad6273-c293-48fc-b44a-f7419da3f866`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `DELETE /projects/:projectId/user-tags/:tagId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-user-tag.md) for the provider-specific parameters and requirements.

