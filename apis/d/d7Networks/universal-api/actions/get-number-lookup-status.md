# D7 Networks: Get Number Lookup Status

Retrieves number lookup status from D7 Networks.

```
GET https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-number-lookup-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-number-lookup-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-number-lookup-status?${params}`, {
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
| `requestId` | string | yes | Request ID returned by the D7 Number Lookup endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "network": "string",
      "ported": true,
      "reachable": true,
      "recipient": "string",
      "status": "string",
      "status_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `network` | string |  |
| `ported` | boolean |  |
| `reachable` | boolean |  |
| `recipient` | string |  |
| `status` | string |  |
| `status_code` | string |  |

## Native endpoint

Through the native D7 Networks API, this operation is `GET /hlr/v1/report/:requestId` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-lookup-status.md) for the provider-specific parameters and requirements.

