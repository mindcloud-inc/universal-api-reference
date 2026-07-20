# Billwerkplus: Get Add-On

Retrieves an add-on from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-add-on
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-add-on?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-add-on?${params}`, {
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
| `handle` | string | yes | Add-on handle. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxRateForCountry` | string | no | Country code to evaluate tax rate for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /add_on/:handle` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-add-on.md) for the provider-specific parameters and requirements.

