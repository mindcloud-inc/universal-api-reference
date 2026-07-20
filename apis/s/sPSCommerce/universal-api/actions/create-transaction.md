# SPS Commerce: Create Transaction

This API accepts a payload that initiates a new transaction.

```
POST https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SPS Commerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filePath` | string | yes | Full absolute path to the file (case sensitive) |
| `payload` | string | no | Example: `This is test data!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "path": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `path` | string | Full absolute path of the created file. |
| `url` | string | URL to download the created file. |

## Native endpoint

Through the native SPS Commerce API, this operation is `POST transactions/v5/data/:filePath` (base URL `https://api.spscommerce.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

