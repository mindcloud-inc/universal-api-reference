# Koncile OCR: Get Folder



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-folder?connectionId=$CONNECTION_ID&folder_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-folder?${params}`, {
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
| `folder_id` | string | yes | The ID of the folder to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "id": 1,
      "name": "Ava Chen",
      "templates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string | The folder description. |
| `id` | number | The folder identifier. |
| `name` | string | The folder name. |
| `templates` | array<object> | Templates linked to the folder. |

## Native endpoint

Through the native Koncile OCR API, this operation is `GET /fetch_folder` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

