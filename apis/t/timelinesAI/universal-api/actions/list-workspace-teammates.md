# TimelinesAI: List Workspace Teammates

Retrieves teammates from your TimelinesAI workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-workspace-teammates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-workspace-teammates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-workspace-teammates?${params}`, {
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
      "data": {
        "teammates": [
          {
            "createdAt": "string",
            "displayName": "Ava Chen",
            "email": "ava@example.com",
            "role": "string",
            "status": "string",
            "userId": 1,
            "whatsappAccounts": [
              {
                "id": "string",
                "phone": "string"
              }
            ]
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.teammates` | array<object> |  |
| `data.teammates[].createdAt` | string |  |
| `data.teammates[].displayName` | string |  |
| `data.teammates[].email` | string |  |
| `data.teammates[].role` | string |  |
| `data.teammates[].status` | string |  |
| `data.teammates[].userId` | number |  |
| `data.teammates[].whatsappAccounts` | array<object> |  |
| `data.teammates[].whatsappAccounts[].id` | string |  |
| `data.teammates[].whatsappAccounts[].phone` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /teammates` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-teammates.md) for the provider-specific parameters and requirements.

