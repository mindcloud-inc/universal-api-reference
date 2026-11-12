# 3E Protect: Remove Catalog Item from Locations



```
DELETE https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/remove-catalog-item-from-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/remove-catalog-item-from-locations?connectionId=$CONNECTION_ID&source=string&identifier=string&locationNames%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string",
  "identifier": "string",
  "locationNames[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/remove-catalog-item-from-locations?${params}`, {
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
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |
| `locationNames[]` | array<string> | yes | Existing 3E location names. Retrieve them with List Locations. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `DELETE /catalog-item-inventory` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-catalog-item-from-locations.md) for the provider-specific parameters and requirements.

