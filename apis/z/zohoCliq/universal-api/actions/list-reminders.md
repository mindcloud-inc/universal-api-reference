# Zoho Cliq: List Reminders

Retrieves all reminders from Zoho Cliq.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-reminders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-reminders?${params}`, {
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
| `category` | string | no | The reminder category to retrieve, such as mine. |
| `limit` | number | no | The number of reminders to retrieve. |
| `nextSetToken` | string | no | Use the token from a previous response to retrieve the next reminder page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "list": [
        {}
      ],
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `list` | array<object> |  |
| `time` | number |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /reminders` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

