# Timeular: List Activities

Retrieves activities from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-activities?${params}`, {
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
      "activities": [
        {
          "color": "string",
          "folderId": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "archivedActivities": [
        {
          "color": "string",
          "folderId": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "inactiveActivities": [
        {
          "color": "string",
          "folderId": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities[].color` | string |  |
| `activities[].folderId` | string |  |
| `activities[].id` | string |  |
| `activities[].name` | string |  |
| `archivedActivities[].color` | string |  |
| `archivedActivities[].folderId` | string |  |
| `archivedActivities[].id` | string |  |
| `archivedActivities[].name` | string |  |
| `inactiveActivities[].color` | string |  |
| `inactiveActivities[].folderId` | string |  |
| `inactiveActivities[].id` | string |  |
| `inactiveActivities[].name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/activities` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

