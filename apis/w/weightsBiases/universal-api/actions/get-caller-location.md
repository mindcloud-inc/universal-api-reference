# Weights & Biases: Get Caller Location

Retrieves caller location details from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-caller-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-caller-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-caller-location?${params}`, {
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
      "allowed": true,
      "ip": "string",
      "location": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed` | boolean | Whether the IP address is allowed for inference. |
| `ip` | string | Resolved IP address. |
| `location` | object | Geolocation details when W&B can resolve the IP address. |

## Native endpoint

Through the native Weights & Biases API, this operation is `GET /geolocate` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-location.md) for the provider-specific parameters and requirements.

