# Harbour: Get Folder

Retrieves a specific folder from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-folder?connectionId=$CONNECTION_ID&folder_id=folder-AbCd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder_id": "folder-AbCd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-folder?${params}`, {
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
| `folder_id` | string | yes | Unique Harbour folder identifier. Example: `folder-AbCd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/folders/:folder_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

