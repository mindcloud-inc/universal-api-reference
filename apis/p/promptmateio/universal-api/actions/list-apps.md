# Promptmate.io: List Apps



```
GET https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-apps?${params}`, {
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
      "appId": "string",
      "appName": "Ava Chen",
      "creditEstimate": 1,
      "dataFields": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Promptmate app ID. |
| `appName` | string | Promptmate app name. |
| `creditEstimate` | number | Estimated credit consumption for an app run. |
| `dataFields` | array<string> | Expected input field names for the app. |

## Native endpoint

Through the native Promptmate.io API, this operation is `GET /apps` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps.md) for the provider-specific parameters and requirements.

