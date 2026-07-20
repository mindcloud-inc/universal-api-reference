# Woodpecker.co: List Campaign Prospects

Retrieves prospects from a Woodpecker campaign.

```
GET https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaign-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaign-prospects?connectionId=$CONNECTION_ID&campaignIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaign-prospects?${params}`, {
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
| `campaignIds` | string | yes | Comma-separated Woodpecker campaign IDs. Accepts multiple values in one string, delimited by `,`. |
| `page` | number | no | Page number. |
| `perPage` | number | no | Number of prospects per page. |
| `sort` | string | no | Woodpecker sort expression. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `GET /rest/v1/prospects` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-prospects.md) for the provider-specific parameters and requirements.

