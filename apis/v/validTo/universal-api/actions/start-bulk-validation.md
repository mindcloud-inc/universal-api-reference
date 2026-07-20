# validTo: Start Bulk Validation

Starts a bulk validation list in validTo.

```
PUT https://connect.mindcloud.co/v1/universal/validTo/latest/actions/start-bulk-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a validTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/start-bulk-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/validTo/latest/actions/start-bulk-validation', {
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
| `jobId` | string | yes | The bulk validation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | The job_id corresponding to the list whose verification was started. |
| `message` | string | Describes the start result. |
| `success` | boolean | Whether the API request call was successful. |

## Native endpoint

Through the native validTo API, this operation is `PATCH /bulk/:jobId` (base URL `https://api.validto.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-bulk-validation.md) for the provider-specific parameters and requirements.

