# EasyPost: Create Batch Scan Form

Creates a scan form for an existing batch in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-scan-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-scan-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-scan-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EasyPost Batch ID, beginning with batch_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mode": "string",
      "object": "string",
      "scanForm": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `scanForm` | object |  |
| `status` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /batches/:id/scan_form` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-scan-form.md) for the provider-specific parameters and requirements.

