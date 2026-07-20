# QuickFile: List Payment Methods



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-payment-methods?${params}`, {
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
| `includeIconPaths` | boolean | no | Include QuickFile icon image paths in the returned payment method records. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iconUrl": "https://example.com",
      "name": "Ava Chen",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iconUrl` | string | QuickFile payment method icon URL when requested. |
| `name` | string | QuickFile payment method display name. |
| `reference` | string | QuickFile payment method code. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /payment/getpaymethods` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-methods.md) for the provider-specific parameters and requirements.

