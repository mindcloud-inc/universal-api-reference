# Deel: Delete Contract Milestone

Deletes an existing contract milestone from Deel.

```
DELETE https://connect.mindcloud.co/v1/universal/deel/latest/actions/delete-contract-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/deel/latest/actions/delete-contract-milestone?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deel/latest/actions/delete-contract-milestone?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Deel API, this operation is `DELETE /contracts/:contract_id/milestones/:milestone_id` (base URL `https://api.letsdeel.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contract-milestone.md) for the provider-specific parameters and requirements.

