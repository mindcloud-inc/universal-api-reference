# GitScrum: Get Workspace Stats

Retrieves statistics for the current GitScrum workspace.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-workspace-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-workspace-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-workspace-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stats` | object |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /companies/stats` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-stats.md) for the provider-specific parameters and requirements.

