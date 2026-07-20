# Onfleet: Get Worker

Retrieves a worker from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-worker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-worker?connectionId=$CONNECTION_ID&workerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-worker?${params}`, {
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
| `workerId` | string | yes | The Onfleet worker ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountStatus": "string",
      "capacity": 1,
      "displayName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "onDuty": true,
      "phone": "string",
      "teams": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountStatus` | string |  |
| `capacity` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `onDuty` | boolean |  |
| `phone` | string |  |
| `teams` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /workers/:workerId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worker.md) for the provider-specific parameters and requirements.

