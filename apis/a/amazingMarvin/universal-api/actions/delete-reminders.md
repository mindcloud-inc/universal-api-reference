# Amazing Marvin: Delete Reminders

Deletes reminders from Amazing Marvin.

```
DELETE https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/delete-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/delete-reminders?connectionId=$CONNECTION_ID&reminderIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reminderIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/delete-reminders?${params}`, {
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
| `reminderIds[]` | array<string> | yes | IDs of reminders to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /reminder/delete` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-reminders.md) for the provider-specific parameters and requirements.

