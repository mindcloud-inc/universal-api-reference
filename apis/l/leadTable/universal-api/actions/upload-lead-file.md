# LeadTable: Upload lead file



```
POST https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upload-lead-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upload-lead-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/upload-lead-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to upload to the lead. |
| `id` | string | yes | The lead that should receive the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native LeadTable API, this operation is `POST /addFile` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-lead-file.md) for the provider-specific parameters and requirements.

