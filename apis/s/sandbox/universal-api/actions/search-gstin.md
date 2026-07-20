# Sandbox: Search GSTIN

Retrieves GST registration details from Sandbox by GSTIN.

```
GET https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sandbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin?connectionId=$CONNECTION_ID&gstin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gstin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin?${params}`, {
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
| `gstin` | string | yes | GSTIN to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "timestamp": 1,
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `timestamp` | number |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native Sandbox API, this operation is `POST /gst/compliance/public/gstin/search` (base URL `https://api.sandbox.co.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-gstin.md) for the provider-specific parameters and requirements.

