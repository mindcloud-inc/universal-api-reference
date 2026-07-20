# Date & Time: List Public Applets For Trigger ID



```
GET https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/list-public-applets-for-trigger-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Date & Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/list-public-applets-for-trigger-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/list-public-applets-for-trigger-id?${params}`, {
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
| `limit` | number | no | Maximum number of applets to return. Default: `10`. |
| `triggerId` | number | no | IFTTT trigger numeric ID used to filter public applets. Default: `3`. |
| `offset` | number | no | Number of applets to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applets` | array<object> | List Public Applets For Trigger ID response root. |

## Native endpoint

Through the native Date & Time API, this operation is `POST api/v3/graph` (base URL `https://ifttt.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-applets-for-trigger-id.md) for the provider-specific parameters and requirements.

