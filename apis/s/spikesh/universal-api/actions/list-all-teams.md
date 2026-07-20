# Spike.sh: List All Teams

Retrieves all teams in your Spike.sh organization.

```
GET https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-all-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spike.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-all-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/list-all-teams?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Spike.sh API returns.

## Native endpoint

Through the native Spike.sh API, this operation is `GET /teams/get-all-teams` (base URL `https://api.spike.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-teams.md) for the provider-specific parameters and requirements.

