# Dify: Get End User Info

Retrieves end-user details from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-end-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-end-user-info?connectionId=$CONNECTION_ID&endUserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endUserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-end-user-info?${params}`, {
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
| `endUserId` | string | yes | End-user ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createdAt": "string",
      "externalUserId": "string",
      "id": "string",
      "isAnonymous": true,
      "name": "Ava Chen",
      "sessionId": "string",
      "tenantId": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createdAt` | string |  |
| `externalUserId` | string |  |
| `id` | string |  |
| `isAnonymous` | boolean |  |
| `name` | string |  |
| `sessionId` | string |  |
| `tenantId` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /end-users/:end_user_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-end-user-info.md) for the provider-specific parameters and requirements.

