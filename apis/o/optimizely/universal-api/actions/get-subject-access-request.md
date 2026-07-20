# Optimizely: Get Subject Access Request

Retrieves a subject access request from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-subject-access-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-subject-access-request?connectionId=$CONNECTION_ID&requestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-subject-access-request?${params}`, {
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
| `requestId` | string | yes | The subject access request id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "completedAtTime": "string",
      "dataType": "string",
      "expiredAtTime": "string",
      "id": 1,
      "identifier": "string",
      "identifierType": "string",
      "requestedAtTime": "string",
      "requestType": "string",
      "slaDeadlineTime": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `completedAtTime` | string |  |
| `dataType` | string |  |
| `expiredAtTime` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `identifierType` | string |  |
| `requestedAtTime` | string |  |
| `requestType` | string |  |
| `slaDeadlineTime` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /subject-access-requests/{requestId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subject-access-request.md) for the provider-specific parameters and requirements.

