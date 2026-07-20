# Sigma: List Source Swap Policies



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-source-swap-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-source-swap-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-source-swap-policies?${params}`, {
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
| `entries` | array<object> | Source swap policy entries |
| `nextPage` | string | Cursor for the next page of source swap policies |
| `total` | number | Total number of source swap policies |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/sourceSwapPolicies` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-source-swap-policies.md) for the provider-specific parameters and requirements.

