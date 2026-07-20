# Moxie: List Project Task Stages

Retrieves project task stages from Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-project-task-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-project-task-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-project-task-stages?${params}`, {
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
      "clientApproval": true,
      "clientApprovalReminderDays": 1,
      "complete": true,
      "hexColor": "string",
      "id": "string",
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientApproval` | boolean |  |
| `clientApprovalReminderDays` | number |  |
| `complete` | boolean |  |
| `hexColor` | string |  |
| `id` | string |  |
| `label` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/taskStages/list` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-task-stages.md) for the provider-specific parameters and requirements.

