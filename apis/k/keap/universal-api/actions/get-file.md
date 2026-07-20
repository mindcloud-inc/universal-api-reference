# Keap: Get File



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-file?connectionId=$CONNECTION_ID&file_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-file?${params}`, {
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
| `file_id` | string | yes | The unique identifier of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "contactId": "string",
      "createdById": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fileBoxType": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "id": "string",
      "isPublic": true,
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `contactId` | string |  |
| `createdById` | string |  |
| `createdTime` | date |  |
| `fileBoxType` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Keap API, this operation is `GET /files/:file_id` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

