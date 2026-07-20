# Incontrol: Get File

Retrieves details for a file from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-file?connectionId=$CONNECTION_ID&id=string&sourceType=string&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "sourceType": "string",
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-file?${params}`, {
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
| `id` | string | yes | The file ID. |
| `sourceType` | string | yes | The origin type of the file (for security purpose). |
| `sourceId` | string | yes | The ID of the origin type of the file (for security purpose). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checksum": "string",
      "extension": "string",
      "id": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum` | string |  |
| `extension` | string |  |
| `id` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/file/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

