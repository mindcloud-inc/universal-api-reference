# remberg: List Organization Contacts

Retrieves contacts for an organization from remberg.

```
GET https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-organization-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a remberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-organization-contacts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-organization-contacts?${params}`, {
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
| `id` | string | yes | Organization ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native remberg API returns.

## Native endpoint

Through the native remberg API, this operation is `GET /v1/organizations/{id}/contacts` (base URL `https://api.remberg.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-contacts.md) for the provider-specific parameters and requirements.

