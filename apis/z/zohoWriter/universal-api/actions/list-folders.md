# Zoho Writer: List Folders

Retrieves folders from Zoho Writer.

```
GET https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-folders?${params}`, {
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
| `category` | string | no | Folder category to list. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folders": [
        {
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folders` | array<object> |  |
| `folders[].role` | string |  |
| `folders[].status` | string |  |
| `folders[].type` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `GET /v1/folders` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

