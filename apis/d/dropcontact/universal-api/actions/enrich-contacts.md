# Dropcontact: Enrich Contacts

Creates a contact enrichment request in Dropcontact.

```
POST https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/enrich-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropcontact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/enrich-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/enrich-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customCallbackUrl` | string | no | Optional per-request webhook callback URL. |
| `data` | list<object> | yes | Contact records to enrich. Dropcontact accepts up to 250 contacts per request. |
| `language` | string | no | Language used by Dropcontact for enrichment heuristics, for example en or fr. |
| `siren` | boolean | no | Whether to return SIREN data when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_left": 1,
      "error": true,
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_left` | number |  |
| `error` | boolean |  |
| `request_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dropcontact API, this operation is `POST /v1/enrich/all` (base URL `https://api.dropcontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-contacts.md) for the provider-specific parameters and requirements.

