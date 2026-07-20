# Seqera: List Runs

Retrieves workflow runs from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-runs?${params}`, {
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
      "nextPageToken": "string",
      "runs": [
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
| `nextPageToken` | string | Pagination token for the next page of runs. |
| `runs` | array<object> | Workflow runs visible to the authenticated user. |

## Native endpoint

Through the native Seqera API, this operation is `GET /ga4gh/wes/v1/runs` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-runs.md) for the provider-specific parameters and requirements.

