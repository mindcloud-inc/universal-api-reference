# OpenSea: Build Criteria Offer

Builds a criteria offer in OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-offer-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-offer-v2?connectionId=$CONNECTION_ID&offerer=string&quantity=1&criteria=%5Bobject%20Object%5D&protocolAddress=string&offerProtectionEnabled=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerer": "string",
  "quantity": "1",
  "criteria": "[object Object]",
  "protocolAddress": "string",
  "offerProtectionEnabled": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-offer-v2?${params}`, {
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
| `offerer` | string | yes |  |
| `quantity` | number | yes |  |
| `criteria` | object | yes |  |
| `protocolAddress` | string | yes |  |
| `offerProtectionEnabled` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `POST /api/v2/offers/build` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-offer-v2.md) for the provider-specific parameters and requirements.

