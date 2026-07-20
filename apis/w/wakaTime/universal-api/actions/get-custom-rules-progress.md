# WakaTime: Get Custom Rules Progress

Retrieves custom rule application progress from WakaTime.

```
GET https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-custom-rules-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WakaTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-custom-rules-progress?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-custom-rules-progress?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native WakaTime API, this operation is `GET /users/:user/custom_rules_progress` (base URL `https://api.wakatime.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-rules-progress.md) for the provider-specific parameters and requirements.

