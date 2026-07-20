# CATS: List Applications By Candidate

Retrieves applications for a candidate in CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-candidate?connectionId=$CONNECTION_ID&candidateId=411876208" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "candidateId": "411876208"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-candidate?${params}`, {
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
| `candidateId` | number | yes | The ID of the candidate to return applications for. Example: `411876208`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `GET /candidates/:candidate_id/applications` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications-by-candidate.md) for the provider-specific parameters and requirements.

