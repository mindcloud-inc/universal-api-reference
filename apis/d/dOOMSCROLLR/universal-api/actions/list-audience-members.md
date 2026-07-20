# DOOMSCROLLR: List Audience Members



```
GET https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-audience-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DOOMSCROLLR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-audience-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-audience-members?${params}`, {
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
| `perPage` | number | no | Maximum number of audience members to return. The docs example uses 100. Default: `100`. Example: `100`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DOOMSCROLLR API returns.

## Native endpoint

Through the native DOOMSCROLLR API, this operation is `GET /api/audience/list` (base URL `https://mindcloudapps0402.doomscrollr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audience-members.md) for the provider-specific parameters and requirements.

