# Stacker: List Stacks

Retrieves stacks from Stacker.

```
GET https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-stacks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-stacks?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-stacks?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "sid": "string",
      "zone_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Stack name. |
| `sid` | string | Stack identifier. |
| `zone_name` | string | Zone or workspace name shown by Stacker. |

## Native endpoint

Through the native Stacker API, this operation is `GET /api/external/stacks/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stacks.md) for the provider-specific parameters and requirements.

