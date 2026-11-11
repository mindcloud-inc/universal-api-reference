# Acumatica: Invoke Opportunity Action



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/invoke-opportunity-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/invoke-opportunity-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webServiceEndpoint": "MindCloudIntegration",
  "endpointVersion": "1.0.0",
  "actionName": "CloseAsLost"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/invoke-opportunity-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webServiceEndpoint": "MindCloudIntegration",
    "endpointVersion": "1.0.0",
    "actionName": "CloseAsLost"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webServiceEndpoint` | string | yes | Name of the Acumatica web service endpoint. Example: `MindCloudIntegration`. |
| `endpointVersion` | string | yes | Version of the web service endpoint. Example: `1.0.0`. |
| `actionName` | string | yes | Name of the opportunity action to run. Example: `CloseAsLost`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Acumatica accepted the operation. |

## Native endpoint

Through the native Acumatica API, this operation is `POST /entity/:webServiceEndpoint/:endpointVersion/Opportunity/:actionName` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invoke-opportunity-action.md) for the provider-specific parameters and requirements.

