# Billetweb: List Session Changes

Retrieves session changes from your Billetweb account.

```
GET https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-session-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-session-changes?connectionId=$CONNECTION_ID&start=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-session-changes?${params}`, {
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
| `start` | number | yes | Return date change entries modified after this Unix timestamp. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | number | no | Optionally return date change entries modified before this Unix timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `GET /date_changes` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-changes.md) for the provider-specific parameters and requirements.

