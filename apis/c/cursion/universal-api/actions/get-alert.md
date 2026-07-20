# Cursion: Get Alert

Retrieves an existing alert from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-alert?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-alert?${params}`, {
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
| `alertId` | string | yes | The alert identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "actions": [
        {}
      ],
      "expressions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "schedule": "string",
      "time_created": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `actions` | array<object> |  |
| `expressions` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `schedule` | string |  |
| `time_created` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /alert/{{alertId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert.md) for the provider-specific parameters and requirements.

