# HelpCrunch: Get Team Availability Status

Retrieves team availability status from HelpCrunch.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-team-availability-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-team-availability-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-team-availability-status?${params}`, {
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
      "chatEnabled": true,
      "domain": "string",
      "id": 1,
      "teamOnline": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatEnabled` | boolean |  |
| `domain` | string |  |
| `id` | number |  |
| `teamOnline` | boolean |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `GET /organization` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-availability-status.md) for the provider-specific parameters and requirements.

