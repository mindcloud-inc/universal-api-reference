# GanttPRO: List Resources

Retrieves resources from your GanttPRO account.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-resources?${params}`, {
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
      "accountRoleId": 1,
      "colorId": 1,
      "customDays": [
        {}
      ],
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "photo": "string",
      "resourceProjects": [
        {}
      ],
      "teamId": 1,
      "userId": 1,
      "workingDays": [
        1
      ],
      "workingHours": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountRoleId` | number |  |
| `colorId` | number |  |
| `customDays` | array<object> |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `photo` | string |  |
| `resourceProjects` | array<object> |  |
| `teamId` | number |  |
| `userId` | number |  |
| `workingDays` | array<number> |  |
| `workingHours` | number |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /resources` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

