# Sendbird: Get Announcement



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-announcement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-announcement?connectionId=$CONNECTION_ID&uniqueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-announcement?${params}`, {
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
| `uniqueId` | string | yes | The unique ID of the announcement. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "state": "string",
      "targetAt": 1,
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `state` | string |  |
| `targetAt` | number |  |
| `uniqueId` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /announcements/:uniqueId` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-announcement.md) for the provider-specific parameters and requirements.

