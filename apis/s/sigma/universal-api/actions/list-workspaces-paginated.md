# Sigma: List Workspaces (Paginated)



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-workspaces-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-workspaces-paginated?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-workspaces-paginated?${params}`, {
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
      "entries": [
        {}
      ],
      "hasMore": true,
      "nextPage": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Workspace entries |
| `hasMore` | boolean | Deprecated pagination hint |
| `nextPage` | string | Cursor for the next page of workspaces |
| `total` | number | Total number of workspaces |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2.1/workspaces` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces-paginated.md) for the provider-specific parameters and requirements.

