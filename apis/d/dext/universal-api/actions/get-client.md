# Dext: Get Client

Retrieves detailed client information from Dext.

```
GET https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dext `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes | The Dext client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertLevel": "string",
      "bankReconciliation": {},
      "healthScore": 1,
      "hmrcStatus": "string",
      "id": "string",
      "metrics": {},
      "name": "Ava Chen",
      "practiceCode": "string",
      "providerName": "Ava Chen",
      "vatDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertLevel` | string |  |
| `bankReconciliation` | object |  |
| `healthScore` | number |  |
| `hmrcStatus` | string |  |
| `id` | string |  |
| `metrics` | object |  |
| `name` | string |  |
| `practiceCode` | string |  |
| `providerName` | string |  |
| `vatDetails` | object |  |

## Native endpoint

Through the native Dext API, this operation is `GET /clients/:client_id` (base URL `https://api.precision.dext.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

