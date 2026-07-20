# Weights & Biases: Get Server Info

Retrieves trace server information from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "min_required_weave_python_version": "string",
      "trace_server_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `min_required_weave_python_version` | string | Minimum required Weave Python package version. |
| `trace_server_version` | string | Trace server version. |

## Native endpoint

Through the native Weights & Biases API, this operation is `GET /server_info` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-info.md) for the provider-specific parameters and requirements.

