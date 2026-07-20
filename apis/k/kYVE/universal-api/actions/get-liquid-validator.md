# KYVE: Get Liquid Validator



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-liquid-validator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-liquid-validator?connectionId=$CONNECTION_ID&validatorAddr=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "validatorAddr": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-liquid-validator?${params}`, {
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
| `validatorAddr` | string | yes | Liquid validator address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "liquid_validator": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `liquid_validator` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/liquid/v1beta1/liquid_validator/{validator_addr}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-liquid-validator.md) for the provider-specific parameters and requirements.

