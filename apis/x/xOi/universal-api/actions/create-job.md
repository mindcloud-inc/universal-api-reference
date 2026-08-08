# XOi: Create Job



```
POST https://connect.mindcloud.co/v1/universal/xOi/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assigneeId": "string",
  "customerName": "Ava Chen",
  "jobLocation": "string",
  "workOrderNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xOi/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assigneeId": "string",
    "customerName": "Ava Chen",
    "jobLocation": "string",
    "workOrderNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | string | yes | XOi assignee id input. |
| `customerName` | string | yes | XOi customer name input. |
| `jobLocation` | string | yes | XOi job location input. |
| `workOrderNumber` | string | yes | XOi work order number input. |
| `label` | string | no | XOi label input. |
| `externalId` | string | no | Optional unique job ID from the external system. |

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
      "deepLinks": {},
      "externalId": "string",
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
| `deepLinks` | object |  |
| `externalId` | string |  |
| `id` | string |  |
| `jobLocation` | string |  |
| `label` | string |  |
| `tags` | array<object> |  |
| `tagSuggestions` | array<object> |  |
| `workOrderNumber` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-jobs-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

