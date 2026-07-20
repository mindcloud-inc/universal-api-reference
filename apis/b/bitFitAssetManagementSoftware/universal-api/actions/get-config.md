# bitFit Asset Management Software: Get Config



```
GET https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/get-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a bitFit Asset Management Software `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/get-config?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/get-config?${params}`, {
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
| `id` | number | yes | The BitFit config ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item` | object | The requested BitFit config. |

## Native endpoint

Through the native bitFit Asset Management Software API, this operation is `GET /v2/configs/:id` (base URL `https://api-assets.bitfit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-config.md) for the provider-specific parameters and requirements.

