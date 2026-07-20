# Zakeke: Duplicate Design



```
POST https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/duplicate-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/duplicate-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "000-RE1olDzbT234viB6D11a10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/duplicate-design', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "000-RE1olDzbT234viB6D11a10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designId` | string | yes | Unique design identifier provided by Zakeke. Example: `000-RE1olDzbT234viB6D11a10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `POST /v2/designs/{designID}` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-design.md) for the provider-specific parameters and requirements.

