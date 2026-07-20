# GrassBlade LRS: Get Person By Agent

Retrieves person details from GrassBlade LRS by agent.

```
GET https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-person-by-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-person-by-agent?connectionId=$CONNECTION_ID&agent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-person-by-agent?${params}`, {
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
| `agent` | string | yes | Agent JSON to fetch person information for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `GET /agents` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-agent.md) for the provider-specific parameters and requirements.

