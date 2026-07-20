# Evalumo: Get Exported Project

Finds an exported project in Evalumo by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/get-exported-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/get-exported-project?connectionId=$CONNECTION_ID&lookup=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookup": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/get-exported-project?${params}`, {
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
| `lookup` | string | yes | Exported project id, original project id, or project name lookup value. |
| `lineItemsToExpand` | string | no | Optional comma-separated line item sections to expand in the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Evalumo API returns.

## Native endpoint

Through the native Evalumo API, this operation is `GET /exportedProject/:lookup` (base URL `https://api.evalumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exported-project.md) for the provider-specific parameters and requirements.

