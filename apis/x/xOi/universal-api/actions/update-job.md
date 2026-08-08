# XOi: Update Job



```
PUT https://connect.mindcloud.co/v1/universal/xOi/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xOi/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | XOi job id input. |
| `customerName` | string | no | XOi customer name input. |
| `jobLocation` | string | no | XOi job location input. |
| `workOrderNumber` | string | no | XOi work order number input. |
| `label` | string | no | XOi label input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeIds": [
        "string"
      ],
      "createdAt": "string",
      "createdBy": "string",
      "customerName": "Ava Chen",
      "id": "string",
      "jobLocation": "string",
      "label": "string",
      "tags": [
        {}
      ],
      "tagSuggestions": [
        {}
      ],
      "workOrderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeIds` | array<string> |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `customerName` | string |  |
| `id` | string |  |
| `jobLocation` | string |  |
| `label` | string |  |
| `tags` | array<object> |  |
| `tagSuggestions` | array<object> |  |
| `workOrderNumber` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-jobs-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

