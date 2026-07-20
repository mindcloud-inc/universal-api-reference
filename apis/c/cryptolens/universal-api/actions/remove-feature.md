# Cryptolens: Remove Feature

Deletes a feature from a license key in Cryptolens.

```
DELETE https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/remove-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/remove-feature?connectionId=$CONNECTION_ID&productId=1&key=string&feature=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1",
  "key": "string",
  "feature": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/remove-feature?${params}`, {
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
| `productId` | number | yes | The product id. |
| `key` | string | yes | The serial key string. |
| `feature` | number | yes | The feature number, 1 to 8 inclusive, that should be removed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Remove Feature acknowledgement message from the Cryptolens result envelope. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/key/RemoveFeature` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-feature.md) for the provider-specific parameters and requirements.

