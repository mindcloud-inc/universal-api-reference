# Browse AI: Get Robot

Retrieves a robot from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot?${params}`, {
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
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "inputParameters": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Robot creation date and time in the form of a Unix timestamp |
| `id` | string | Unique robot ID |
| `inputParameters` | array<object> |  |
| `name` | string | Robot name |

## Native endpoint

Through the native Browse AI API, this operation is `GET /robots/:robotId` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-robot.md) for the provider-specific parameters and requirements.

