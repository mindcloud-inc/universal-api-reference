# Middesk: Retrieve a business batch

Retrieves a business batch from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-batch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-batch?${params}`, {
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
| `id` | string | yes | Business batch ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "businessCount": 1,
      "completedBusinessCount": 1,
      "createdAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `businessCount` | number |  |
| `completedBusinessCount` | number |  |
| `createdAt` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /business_batches/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-batch.md) for the provider-specific parameters and requirements.

