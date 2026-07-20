# Billetweb: List CRM Contacts

Retrieves CRM contacts from your Billetweb account.

```
GET https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-crm-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-crm-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-crm-contacts?${params}`, {
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
| `lastUpdate` | number | no | Only return contacts updated after this Unix timestamp. |
| `since` | number | no | Only return contacts updated during the last N minutes. |
| `to` | number | no | Only return contacts modified before this Unix timestamp. |
| `email` | string | no | Filter by buyer email. |
| `segment` | number | no | Filter by CRM segment identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `GET /crm/contacts` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crm-contacts.md) for the provider-specific parameters and requirements.

