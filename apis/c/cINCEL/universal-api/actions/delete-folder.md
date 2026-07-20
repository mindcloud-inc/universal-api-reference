# CINCEL: Delete Folder



```
DELETE https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/delete-folder?connectionId=$CONNECTION_ID&team=string&folder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "folder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/delete-folder?${params}`, {
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
| `team` | string | yes | UUID of the team that owns the folder. |
| `folder` | string | yes | UUID of the folder to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": "string",
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | string | UUID of the deleted folder. |
| `message` | string | Provider confirmation message for the deleted folder. |
| `statusCode` | number | HTTP-style status code returned by the delete operation. |

## Native endpoint

Through the native CINCEL API, this operation is `DELETE /teams/:team/folders/:folder` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

