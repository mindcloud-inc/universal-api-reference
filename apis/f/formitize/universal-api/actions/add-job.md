# Formitize: Add Job

Creates a new job in Formitize.

```
POST https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "agentID": true,
      "clientID": 1,
      "contactID": 1,
      "jobID": 1,
      "jobNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentID` | boolean |  |
| `clientID` | number |  |
| `contactID` | number |  |
| `jobID` | number |  |
| `jobNumber` | number |  |

## Native endpoint

Through the native Formitize API, this operation is `POST /job/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-job.md) for the provider-specific parameters and requirements.

