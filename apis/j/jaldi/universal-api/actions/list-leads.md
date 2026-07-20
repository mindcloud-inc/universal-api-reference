# Jaldi: List Leads

Retrieves leads from Jaldi.

```
GET https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaldi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads?${params}`, {
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
| `lastUpdateFrom` | string | no | Return leads updated on or after this Jaldi datetime in YYYY-MM-DD hh:mm format. |
| `lastUpdateTo` | string | no | Return leads updated on or before this Jaldi datetime in YYYY-MM-DD hh:mm format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "notes": "string",
      "phone": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Provisional Jaldi lead email attribute inferred from Jaldi's webhook create contract. |
| `firstName` | string | Provisional Jaldi lead first name attribute inferred from Jaldi's public lead-entry docs and webhook create contract. |
| `lastName` | string | Provisional Jaldi lead last name attribute inferred from Jaldi's webhook create contract. |
| `notes` | string | Provisional Jaldi lead notes attribute inferred from Jaldi's public lead-management docs. |
| `phone` | string | Provisional Jaldi lead phone number attribute inferred from Jaldi's public lead-entry docs. |
| `status` | string | Provisional Jaldi lead status attribute inferred from Jaldi's public lead-status documentation. |
| `updatedAt` | string | Provisional Jaldi lead update timestamp attribute inferred from the fetch endpoint's last_update_from / last_update_to selectors. |

## Native endpoint

Through the native Jaldi API, this operation is `POST /add_on/webhook/fetch_crm_data` (base URL `https://api.jalditech.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

