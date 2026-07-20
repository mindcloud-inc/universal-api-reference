# Nexiopay: Get APM iframe



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/get-apm-iframe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/get-apm-iframe?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/get-apm-iframe?${params}`, {
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
| `token` | string | yes | APM one-time-use token returned by the APM token endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Raw iframe HTML returned by Nexio. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /apm/v3` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-apm-iframe.md) for the provider-specific parameters and requirements.

