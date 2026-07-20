# 2Smart Cloud: Check if user has biometric key



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-users-check-biometric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-users-check-biometric?connectionId=$CONNECTION_ID&device_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "device_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-users-check-biometric?${params}`, {
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
| `device_id` | string | yes | Unique id of device |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string | Provider response message |
| `success` | boolean | Whether the request completed successfully |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /users/check/biometric` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users-check-biometric.md) for the provider-specific parameters and requirements.

