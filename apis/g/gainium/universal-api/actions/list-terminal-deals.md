# Gainium: List Terminal Deals



```
GET https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-terminal-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gainium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-terminal-deals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-terminal-deals?${params}`, {
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
| `botId` | string | no | Filter by bot ID. |
| `fields` | string | no | Field selection preset or custom field list. |
| `page` | number | no | 1-based page number. |
| `status` | list | no | Filter by deal status. One of: `0`, `1`, `2`, `3`, `4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gainium API returns.

## Native endpoint

Through the native Gainium API, this operation is `GET /api/v2/deals/terminal` (base URL `https://api.gainium.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-terminal-deals.md) for the provider-specific parameters and requirements.

