# Testomato: Project notifications

Retrieves project notification settings from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-notifications?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-notifications?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": true,
      "pagerduty": true,
      "pushbullet": true,
      "pushover": true,
      "severity": 1,
      "slack": true,
      "webhook": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | boolean |  |
| `pagerduty` | boolean |  |
| `pushbullet` | boolean |  |
| `pushover` | boolean |  |
| `severity` | number |  |
| `slack` | boolean |  |
| `webhook` | boolean |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/notifications` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-notifications.md) for the provider-specific parameters and requirements.

