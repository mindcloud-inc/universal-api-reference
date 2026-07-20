# Print.one Postcards: Delete Custom File

Deletes an existing custom file from Print.one Postcards.

```
DELETE https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-custom-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-custom-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-custom-file?${params}`, {
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
| `fileId` | string | yes | The ID of the custom file |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "id": "string",
      "metadata": {
        "height": "string",
        "type": "string",
        "width": "string"
      },
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `metadata.height` | string |  |
| `metadata.type` | string |  |
| `metadata.width` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `DELETE /v2/customfiles/[:fileId]` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-file.md) for the provider-specific parameters and requirements.

