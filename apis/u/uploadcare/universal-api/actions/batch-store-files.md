# Uploadcare: Batch Store Files

Stores multiple files in Uploadcare storage.

```
PUT https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-store-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-store-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-store-files', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuids[]` | array<string> | yes | List of Uploadcare file UUIDs to store. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "problems": {},
      "result": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `problems` | object | Per-file problems returned by Uploadcare when present. |
| `result` | array<object> | Stored file records returned by Uploadcare. |
| `status` | string | Batch operation status. |

## Native endpoint

Through the native Uploadcare API, this operation is `PUT /files/storage/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-store-files.md) for the provider-specific parameters and requirements.

