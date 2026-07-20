# Timeular: V3 List all Activities

Retrieves activities from the Timeular v3 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-list-all-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-list-all-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-list-all-activities?${params}`, {
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
          "deviceSide": "string",
          "id": "string",
          "integration": "string",
          "name": "Ava Chen",
          "spaceId": "string"
        }
      ],
      "archivedActivities": [
        {
          "color": "string",
          "id": "string",
          "integration": "string",
          "name": "Ava Chen",
          "spaceId": "string"
        }
      ],
      "inactiveActivities": [
        {
          "color": "string",
          "id": "string",
          "integration": "string",
          "name": "Ava Chen",
          "spaceId": "string"
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
| `activities[].deviceSide` | string |  |
| `activities[].id` | string |  |
| `activities[].integration` | string |  |
| `activities[].name` | string |  |
| `activities[].spaceId` | string |  |
| `archivedActivities[].color` | string |  |
| `archivedActivities[].id` | string |  |
| `archivedActivities[].integration` | string |  |
| `archivedActivities[].name` | string |  |
| `archivedActivities[].spaceId` | string |  |
| `inactiveActivities[].color` | string |  |
| `inactiveActivities[].id` | string |  |
| `inactiveActivities[].integration` | string |  |
| `inactiveActivities[].name` | string |  |
| `inactiveActivities[].spaceId` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v3/activities` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-list-all-activities.md) for the provider-specific parameters and requirements.

