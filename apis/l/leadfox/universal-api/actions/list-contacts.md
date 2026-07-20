# Leadfox: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/list-contacts?${params}`, {
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
| `list` | string | no | Optional Leadfox list identifier to restrict contacts. Example: `123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadfox API returns.

## Native endpoint

Through the native Leadfox API, this operation is `POST /contact/getlist/` (base URL `https://app.leadfox.co/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

