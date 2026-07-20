# Grafana: Get Folder Permissions

Retrieves folder permissions from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-folder-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-folder-permissions?connectionId=$CONNECTION_ID&folderUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-folder-permissions?${params}`, {
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
| `folderUid` | string | yes | The folder UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "permission": "string",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `permission` | string |  |
| `roleName` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /folders/:folder_uid/permissions` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-permissions.md) for the provider-specific parameters and requirements.

