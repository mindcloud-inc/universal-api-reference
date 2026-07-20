# Dubsado: List Scheduler Dropdown Options (Session Required)



```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-scheduler-dropdown-options-session-required
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-scheduler-dropdown-options-session-required?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-scheduler-dropdown-options-session-required?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "emailTemplate": {
        "body": "ava@example.com",
        "subject": "ava@example.com"
      },
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailTemplate.body` | string |  |
| `emailTemplate.subject` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dubsado API, this operation is `GET /scheduler/dropdown/list` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scheduler-dropdown-options-session-required.md) for the provider-specific parameters and requirements.

