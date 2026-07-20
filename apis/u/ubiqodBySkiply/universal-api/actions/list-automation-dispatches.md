# Ubiqod by Skiply: List Automation Dispatches



```
GET https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-automation-dispatches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-automation-dispatches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-automation-dispatches?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Dispatch type. Defaults to POWERAUTOMATE in Ubiqod's connector definition. Default: `POWERAUTOMATE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appType": "string",
      "id": "string",
      "isEnable": true,
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appType` | string | Dispatch application type. |
| `id` | string | Dispatch ID. |
| `isEnable` | boolean | Whether the dispatch is enabled. |
| `label` | string | Dispatch label. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `GET /dispatchs/` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-automation-dispatches.md) for the provider-specific parameters and requirements.

