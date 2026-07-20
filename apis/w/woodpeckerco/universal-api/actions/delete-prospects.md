# Woodpecker.co: Delete Prospects

Deletes prospects from Woodpecker or removes them from campaigns.

```
DELETE https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/delete-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/delete-prospects?connectionId=$CONNECTION_ID&prospectIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prospectIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/delete-prospects?${params}`, {
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
| `campaignIds` | string | no | Campaign IDs to remove the prospects from without deleting them globally. Accepts multiple values in one string, delimited by `,`. |
| `prospectIds` | string | yes | Comma-separated Woodpecker prospect IDs to delete. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `DELETE /rest/v1/prospects` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-prospects.md) for the provider-specific parameters and requirements.

