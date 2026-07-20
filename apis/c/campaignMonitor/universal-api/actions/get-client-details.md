# Campaign Monitor: Get Client Details

Retrieves details for a Campaign Monitor client.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-client-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-client-details?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-client-details?${params}`, {
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
| `clientId` | string | yes | Campaign Monitor client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "basicDetails": {},
      "billingDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | Campaign Monitor API key for the client. |
| `basicDetails` | object | Basic details for the Campaign Monitor client. |
| `billingDetails` | object | Billing details for the Campaign Monitor client. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /clients/:clientId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-details.md) for the provider-specific parameters and requirements.

