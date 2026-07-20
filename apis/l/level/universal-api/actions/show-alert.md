# Level: Show Alert

Retrieves an existing alert from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/show-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/show-alert?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/show-alert?${params}`, {
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
| `id` | string | yes | The ID of the alert to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "deviceHostname": "Ava Chen",
      "deviceId": "string",
      "id": "string",
      "isResolved": true,
      "name": "Ava Chen",
      "resolvedAt": "string",
      "severity": "string",
      "startedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `deviceHostname` | string |  |
| `deviceId` | string |  |
| `id` | string |  |
| `isResolved` | boolean |  |
| `name` | string |  |
| `resolvedAt` | string |  |
| `severity` | string |  |
| `startedAt` | string |  |

## Native endpoint

Through the native Level API, this operation is `GET /alerts/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-alert.md) for the provider-specific parameters and requirements.

