# Quantcast: List Creative Assignments

Retrieves creative assignments from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creative-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creative-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-creative-assignments?${params}`, {
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
      "creativeAssignments": {
        "edges": {
          "adSetId": 1,
          "creativeId": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creativeAssignments` | object | Creative assignments connection returned by Quantcast. |
| `creativeAssignments.edges` | array<object> | Creative assignment nodes in the result set. |
| `creativeAssignments.edges.adSetId` | number | Ad set identifier linked to the creative. |
| `creativeAssignments.edges.creativeId` | number | Creative identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-creative-assignments.md) for the provider-specific parameters and requirements.

