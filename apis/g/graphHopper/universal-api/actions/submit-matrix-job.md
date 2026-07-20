# GraphHopper: Submit Matrix Job

Submits a matrix job in GraphHopper.

```
POST https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/submit-matrix-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/submit-matrix-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/submit-matrix-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestBody` | object | yes | Asynchronous matrix request JSON body matching GraphHopper's MatrixRequest or SymmetricalMatrixRequest schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | Submitted matrix job ID. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /matrix/calculate` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-matrix-job.md) for the provider-specific parameters and requirements.

