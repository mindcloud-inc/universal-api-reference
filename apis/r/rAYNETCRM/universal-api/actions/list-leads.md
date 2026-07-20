# RAYNET CRM: List Leads



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-leads?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "countryCode": "string"
      },
      "code": "string",
      "companyName": "Ava Chen",
      "contactInfo": {
        "email": "ava@example.com",
        "tel1": "string",
        "www": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "leadDate": "2026-05-07T12:00:00.000Z",
      "leadPerson": true,
      "leadPhase": {
        "code01": "string",
        "id": 1
      },
      "owner": {
        "fullName": "Ava Chen",
        "id": 1
      },
      "priority": "string",
      "rowInfo": {
        "createdAt": "string"
      },
      "securityLevel": {
        "name": "Ava Chen"
      },
      "status": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string | Lead city. |
| `address.countryCode` | string | Lead country code. |
| `code` | string | Lead code. |
| `companyName` | string | Company name captured directly on the lead. |
| `contactInfo.email` | string | Lead email address. |
| `contactInfo.tel1` | string | Primary lead phone number. |
| `contactInfo.www` | string | Lead website URL. |
| `firstName` | string | Lead first name. |
| `id` | number | Raynet lead identifier. |
| `lastName` | string | Lead last name. |
| `leadDate` | date | Lead creation date. |
| `leadPerson` | boolean | Whether the lead represents a person. |
| `leadPhase.code01` | string | Lead phase label. |
| `leadPhase.id` | number | Lead phase identifier. |
| `owner.fullName` | string | Assigned owner full name. |
| `owner.id` | number | Assigned owner identifier. |
| `priority` | string | Lead priority. |
| `rowInfo.createdAt` | string | Record creation timestamp. |
| `securityLevel.name` | string | Assigned security level name. |
| `status` | string | Lead lifecycle status. |
| `topic` | string | Lead topic or summary. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET lead/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

