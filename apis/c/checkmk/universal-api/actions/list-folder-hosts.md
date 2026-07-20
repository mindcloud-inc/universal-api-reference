# Checkmk: List Folder Hosts

Retrieves host records from a Checkmk folder.

```
GET https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-folder-hosts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-folder-hosts?connectionId=$CONNECTION_ID&folder=~" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder": "~"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-folder-hosts?${params}`, {
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
| `folder` | string | yes | Folder path or slug, such as ~ for Main or ~linux for the Linux folder. Example: `~`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "links": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `links` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `GET /objects/folder_config/{folder}/collections/hosts` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-hosts.md) for the provider-specific parameters and requirements.

