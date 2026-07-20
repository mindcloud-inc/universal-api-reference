# Framework360: Get Report



```
GET https://connect.mindcloud.co/v1/universal/framework360/latest/actions/reports-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/reports-get?connectionId=$CONNECTION_ID&category=string&item=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string",
  "item": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/reports-get?${params}`, {
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
| `category` | string | yes | Report category. |
| `item` | string | yes | Specific report item. |
| `filters` | object | no | Report filters. |
| `sort[]` | array<string> | no | Sort configuration. |
| `type` | string | yes | Report output type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST reports/get` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reports-get.md) for the provider-specific parameters and requirements.

