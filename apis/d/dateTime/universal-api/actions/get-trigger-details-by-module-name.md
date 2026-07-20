# Date & Time: Get Trigger Details By Module Name



```
GET https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-trigger-details-by-module-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Date & Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-trigger-details-by-module-name?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-trigger-details-by-module-name?${params}`, {
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
| `moduleName` | string | no | Full IFTTT trigger module name such as date_and_time.every_day_at. Default: `date_and_time.every_day_at`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trigger` | object | Get Trigger Details By Module Name response root. |

## Native endpoint

Through the native Date & Time API, this operation is `POST api/v3/graph` (base URL `https://ifttt.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trigger-details-by-module-name.md) for the provider-specific parameters and requirements.

