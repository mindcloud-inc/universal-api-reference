# Kiwili: Get Task Details

Retrieves details for a task in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-task-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-task-details?connectionId=$CONNECTION_ID&task_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-task-details?${params}`, {
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
| `task_id` | number | yes | The Kiwili task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Archive": true,
      "EnterpriseId": 1,
      "Id": 1,
      "ProjectId": 1,
      "Status": "string",
      "Summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Archive` | boolean |  |
| `EnterpriseId` | number |  |
| `Id` | number |  |
| `ProjectId` | number |  |
| `Status` | string |  |
| `Summary` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /task/:task_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-details.md) for the provider-specific parameters and requirements.

