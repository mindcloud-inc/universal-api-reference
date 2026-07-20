# Zakeke: Retrieve Composition By ID



```
GET https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-composition-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-composition-by-id?connectionId=$CONNECTION_ID&compositionId=000-RE1olDzbT234viB6D11a10&quantity=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "compositionId": "000-RE1olDzbT234viB6D11a10",
  "quantity": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-composition-by-id?${params}`, {
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
| `compositionId` | string | yes | Unique configuration identifier provided by Zakeke. Example: `000-RE1olDzbT234viB6D11a10`. |
| `quantity` | number | yes | Quantity used to calculate composition pricing and totals. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `GET /v2/compositions/{compositionID}/{quantity}` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-composition-by-id.md) for the provider-specific parameters and requirements.

