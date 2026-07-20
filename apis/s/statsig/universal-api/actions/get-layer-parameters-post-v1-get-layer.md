# Statsig: Get Layer Parameters

Retrieves layer parameters from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-layer-parameters-post-v1-get-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-layer-parameters-post-v1-get-layer?connectionId=$CONNECTION_ID&layerName=Ava%20Chen&user=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerName": "Ava Chen",
  "user": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-layer-parameters-post-v1-get-layer?${params}`, {
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
| `layerName` | string | yes | Name of the layer. |
| `user` | object | yes | Statsig user object containing at least one identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statsigMetadata` | object | no | SDK metadata for diagnostics and exposure behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocatedExperimentName": "Ava Chen",
      "name": "Ava Chen",
      "ruleID": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedExperimentName` | string | Allocated experiment name, when present. |
| `name` | string | Layer name. |
| `ruleID` | string | Evaluated rule ID. |
| `value` | object | Layer parameter values. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/get_layer` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-layer-parameters-post-v1-get-layer.md) for the provider-specific parameters and requirements.

