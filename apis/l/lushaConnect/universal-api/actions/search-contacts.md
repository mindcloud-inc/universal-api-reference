# Lusha Connect: Search Contacts

Finds contacts in Lusha Connect by enrichment inputs.

```
GET https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lusha Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-contacts?connectionId=$CONNECTION_ID&contacts=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contacts": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-contacts?${params}`, {
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
| `contacts` | list<object> | yes | List of contact lookup objects. Each item must include contactId and one supported lookup combination such as email, linkedinUrl, or fullName with companies. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Lusha Connect API returns.

## Native endpoint

Through the native Lusha Connect API, this operation is `POST /v2/person` (base URL `https://api.lusha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

