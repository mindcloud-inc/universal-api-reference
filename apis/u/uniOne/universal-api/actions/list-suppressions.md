# UniOne: List Suppressions

Retrieves suppressions from UniOne with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-suppressions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-suppressions?${params}`, {
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
| `cause` | string | no | Optional suppression cause filter. Example: `unsubscribed`. |
| `source` | string | no | Optional suppression source filter. Example: `user`. |
| `startTime` | string | no | Optional UTC start time in YYYY-MM-DD hh:mm:ss format. Example: `2026-04-02 00:00:00`. |
| `cursor` | string | no | Continuation cursor from the previous suppression list response. Example: `Ajfb6Hvdkn3hdhhvG57xbdufhG5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST suppression/list.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppressions.md) for the provider-specific parameters and requirements.

