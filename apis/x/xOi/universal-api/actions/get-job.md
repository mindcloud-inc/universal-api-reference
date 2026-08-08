# XOi: Get Job



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=Enter%20an%20XOi%20Vision%20Job%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "Enter an XOi Vision Job ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | The unique XOi Vision Job ID. Example: `Enter an XOi Vision Job ID`. |

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
| `id` | string |  |
| `jobLocation` | string |  |
| `label` | string |  |
| `tags` | array<object> |  |
| `tagSuggestions` | array<object> |  |
| `workOrderNumber` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-jobs-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

