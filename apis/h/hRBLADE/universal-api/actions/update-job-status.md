# HRBLADE: Update Job Status



```
PUT https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Active status flag. |
| `jobId` | number | yes | Job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": true,
      "response": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | boolean |  |
| `response.message` | string |  |

## Native endpoint

Through the native HRBLADE API, this operation is `POST /job/active` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-status.md) for the provider-specific parameters and requirements.

