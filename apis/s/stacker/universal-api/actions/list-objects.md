# Stacker: List Objects

Retrieves objects from Stacker.

```
GET https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-objects?connectionId=$CONNECTION_ID&accountId=string&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-objects?${params}`, {
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
| `accountId` | string | yes | Stacker account ID sent as the X-Account-Id header. |
| `stackId` | string | yes | Stacker stack ID sent as the X-Stack-Id header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "sid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Object name. |
| `sid` | string | Object SID. |

## Native endpoint

Through the native Stacker API, this operation is `GET /api/external/objects/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-objects.md) for the provider-specific parameters and requirements.

