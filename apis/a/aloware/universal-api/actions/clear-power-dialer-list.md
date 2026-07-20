# Aloware: Clear Power Dialer List

Clears all contacts from an Aloware power dialer list.

```
DELETE https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-power-dialer-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-power-dialer-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-power-dialer-list?${params}`, {
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
| `listId` | string | yes | Power dialer list ID to clear. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aloware API returns.

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/powerdialer-clear-list` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-power-dialer-list.md) for the provider-specific parameters and requirements.

