# ipdata.co: Get Caller IP Selected Fields



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-selected-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-selected-fields?connectionId=$CONNECTION_ID&fields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-selected-fields?${params}`, {
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
| `fields` | string | yes | Comma-separated response fields to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ipdata.co API returns.

## Native endpoint

Through the native ipdata.co API, this operation is `GET /` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-ip-selected-fields.md) for the provider-specific parameters and requirements.

