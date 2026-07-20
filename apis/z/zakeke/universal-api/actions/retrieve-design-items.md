# Zakeke: Retrieve Design Items



```
GET https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-design-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-design-items?connectionId=$CONNECTION_ID&designId=000-RE1olDzbT234viB6D11a10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "000-RE1olDzbT234viB6D11a10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-design-items?${params}`, {
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
| `designId` | string | yes | Unique design identifier provided by Zakeke. Example: `000-RE1olDzbT234viB6D11a10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `GET /v1/designs/{designID}/items` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-design-items.md) for the provider-specific parameters and requirements.

