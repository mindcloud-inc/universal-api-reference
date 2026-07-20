# Goodbarber eCommerce: Delete Variant Option



```
DELETE https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/delete-variant-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/delete-variant-option?connectionId=$CONNECTION_ID&optionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "optionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/delete-variant-option?${params}`, {
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
| `optionId` | number | yes | Variant option ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the variant option delete request completed. |
| `id` | number | Deleted variant option ID. |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `DELETE /publicapi/v2/general/catalog/:webzine_id/option/:option_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-variant-option.md) for the provider-specific parameters and requirements.

