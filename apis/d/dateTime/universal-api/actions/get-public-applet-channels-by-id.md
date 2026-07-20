# Date & Time: Get Public Applet Channels By ID



```
GET https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-public-applet-channels-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Date & Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-public-applet-channels-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-public-applet-channels-by-id?${params}`, {
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
| `appletId` | string | no | IFTTT public applet ID. Default: `A5Gtmb9N`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applet` | object | Get Public Applet Channels By ID response root. |

## Native endpoint

Through the native Date & Time API, this operation is `POST api/v3/graph` (base URL `https://ifttt.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-applet-channels-by-id.md) for the provider-specific parameters and requirements.

