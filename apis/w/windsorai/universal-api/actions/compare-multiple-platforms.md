# Windsor.ai: Compare Multiple Platforms

Retrieves cross-platform connector data from Windsor.ai.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/compare-multiple-platforms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/compare-multiple-platforms?connectionId=$CONNECTION_ID&fields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/compare-multiple-platforms?${params}`, {
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
| `datePreset` | string | no | Relative date window such as last_7d or last_30d. |
| `fields` | string | yes | Comma-separated list of Windsor.ai fields to retrieve. |
| `filter` | string | no | JSON filter expression for Windsor.ai connector queries. |
| `maxRows` | string | no | Maximum number of rows to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Windsor.ai API returns.

## Native endpoint

Through the native Windsor.ai API, this operation is `GET https://connectors.windsor.ai/all` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-multiple-platforms.md) for the provider-specific parameters and requirements.

