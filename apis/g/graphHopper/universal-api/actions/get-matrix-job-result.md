# GraphHopper: Get Matrix Job Result

Retrieves a matrix job result from GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-matrix-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-matrix-job-result?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-matrix-job-result?${params}`, {
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
| `jobId` | string | yes | Matrix computation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "solution": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `solution` | object | Matrix response when finished. |
| `status` | string | Matrix job status. |

## Native endpoint

Through the native GraphHopper API, this operation is `GET /matrix/solution/:jobId` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-matrix-job-result.md) for the provider-specific parameters and requirements.

