# Recooty: Get Job



```
GET https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recooty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | The Recooty job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "job": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company name returned by Recooty. |
| `job` | object | The requested job record. |

## Native endpoint

Through the native Recooty API, this operation is `GET /v1/jobs/{{credentials.jobListingKey}}/{{jobId}}` (base URL `https://standaloneapi.recooty.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

