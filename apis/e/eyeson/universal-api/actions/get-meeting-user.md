# Eyeson: Get Meeting User



```
GET https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/get-meeting-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eyeson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/get-meeting-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/get-meeting-user?${params}`, {
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
| `accessKey` | string | no |  |
| `userId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eyeson API returns.

## Native endpoint

Through the native Eyeson API, this operation is `GET /rooms/:accessKey/users/:userId` (base URL `https://api.eyeson.team`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-user.md) for the provider-specific parameters and requirements.

