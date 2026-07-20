# Wrangle: Get Inbox



```
GET https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inbox?connectionId=$CONNECTION_ID&inboxId=inbox_uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "inbox_uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inbox?${params}`, {
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
| `inboxId` | string | yes | The Wrangle inbox ID. Example: `inbox_uuid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inbox": {
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
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inbox.createdAt` | string |  |
| `inbox.creatorId` | string |  |
| `inbox.defaultUserRole` | string |  |
| `inbox.description` | object |  |
| `inbox.id` | string |  |
| `inbox.name` | string |  |
| `inbox.status` | string |  |
| `inbox.updatedAt` | string |  |
| `inbox.userRoles[].role` | string |  |
| `inbox.userRoles[].userId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wrangle API, this operation is `GET /inboxes/:inboxId` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox.md) for the provider-specific parameters and requirements.

