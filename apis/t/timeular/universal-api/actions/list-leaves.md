# Timeular: List Leaves

Retrieves leave requests from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-leaves
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-leaves?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-leaves?${params}`, {
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
      "timeLeaves": [
        {
          "endDate": "string",
          "id": "string",
          "note": "string",
          "startDate": "string",
          "status": "string",
          "typeId": "string",
          "user": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          }
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
| `timeLeaves[].endDate` | string |  |
| `timeLeaves[].id` | string |  |
| `timeLeaves[].note` | string |  |
| `timeLeaves[].startDate` | string |  |
| `timeLeaves[].status` | string |  |
| `timeLeaves[].typeId` | string |  |
| `timeLeaves[].user.email` | string |  |
| `timeLeaves[].user.id` | string |  |
| `timeLeaves[].user.name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/leaves` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leaves.md) for the provider-specific parameters and requirements.

