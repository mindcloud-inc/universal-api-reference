# SuperMCP: Get Campaign Resources



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-campaign-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-campaign-resources?connectionId=$CONNECTION_ID&dataSourceId=string&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string",
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-campaign-resources?${params}`, {
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
| `dataSourceId` | string | yes | Ad platform data source code: AW, FA, AC, TIK, or LIA. |
| `accountId` | string | yes | Platform ad account ID from Discover Accounts. |
| `resourceType` | string | no | Resource to query: campaigns, health_check, assets, pages, posts, keyword_ideas, keyword_volumes, targeting_search, reach_estimate, audiences, recommendations, history, or conversions. Default: `campaigns`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params` | object | no | Resource-type-specific parameters as documented by Supermetrics. |
| `maxRows` | number | no | Maximum resources to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notes": [
        "string"
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notes` | array<string> | Provider notes. |
| `results` | array<object> | Campaign or resource results. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/campaign_and_resource_get` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-resources.md) for the provider-specific parameters and requirements.

