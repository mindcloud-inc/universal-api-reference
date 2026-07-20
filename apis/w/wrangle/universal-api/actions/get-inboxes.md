# Wrangle: Get Inboxes



```
GET https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes?${params}`, {
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
      "inboxes": [
        {
          "createdAt": "string",
          "creatorId": "string",
          "defaultUserRole": "string",
          "description": {},
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "updatedAt": "string",
          "userRoles": [
            {
              "role": "string",
              "userId": "string"
            }
          ]
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inboxes[].createdAt` | string |  |
| `inboxes[].creatorId` | string |  |
| `inboxes[].defaultUserRole` | string |  |
| `inboxes[].description` | object |  |
| `inboxes[].id` | string |  |
| `inboxes[].name` | string |  |
| `inboxes[].status` | string |  |
| `inboxes[].updatedAt` | string |  |
| `inboxes[].userRoles[].role` | string |  |
| `inboxes[].userRoles[].userId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wrangle API, this operation is `GET /inboxes` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inboxes.md) for the provider-specific parameters and requirements.

