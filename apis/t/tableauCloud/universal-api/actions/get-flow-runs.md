# Tableau Cloud: Get Flow Runs

Retrieves flow runs from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-flow-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-flow-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-flow-runs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundJobId": "string",
      "completedAt": "string",
      "flowId": "string",
      "id": "string",
      "progress": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundJobId` | string | Background job ID. |
| `completedAt` | string | Completion timestamp. |
| `flowId` | string | Flow ID. |
| `id` | string | Flow run ID. |
| `progress` | string | Progress percentage. |
| `startedAt` | string | Start timestamp. |
| `status` | string | Flow run status. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/flows/runs` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-flow-runs.md) for the provider-specific parameters and requirements.

