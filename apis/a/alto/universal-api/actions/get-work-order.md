# Alto: Get Work Order

Retrieves a work order from Alto by ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-work-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-work-order?${params}`, {
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
| `id` | string | yes | Unique Alto work order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "propertyId": "string",
      "reportedDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `propertyId` | string |  |
| `reportedDate` | date |  |
| `startDate` | date |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /work-orders/:id` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-order.md) for the provider-specific parameters and requirements.

