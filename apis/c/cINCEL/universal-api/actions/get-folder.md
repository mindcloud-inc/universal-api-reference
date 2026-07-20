# CINCEL: Get Folder



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-folder?connectionId=$CONNECTION_ID&team=string&folder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "folder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-folder?${params}`, {
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
| `folder` | string | yes | UUID of the folder to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "team": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Folder creation timestamp. |
| `deletedAt` | date | Deletion timestamp when the folder has been deleted. |
| `name` | string | Folder name. |
| `team` | string | Owning team UUID. |
| `updatedAt` | date | Folder last update timestamp. |
| `uuid` | string | Folder UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/folders/:folder` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

