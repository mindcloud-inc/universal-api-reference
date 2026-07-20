# RAYNET CRM: List Companies



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-companies?${params}`, {
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
      "birthday": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "owner": {
        "fullName": "Ava Chen",
        "id": 1
      },
      "paymentTerm": {
        "value": "string"
      },
      "person": true,
      "primaryAddress": {
        "address": {
          "city": "string",
          "country": "string",
          "countryCode": "string"
        },
        "contactInfo": {
          "email": "ava@example.com",
          "www": "string"
        }
      },
      "rating": "string",
      "regNumber": "string",
      "role": "string",
      "rowInfo": {
        "createdAt": "2026-05-07T12:00:00.000Z"
      },
      "securityLevel": {
        "name": "Ava Chen"
      },
      "state": "string",
      "taxNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | date | Stored company birthday or anniversary date. |
| `id` | number | Raynet company identifier. |
| `name` | string | Company display name. |
| `owner.fullName` | string | Assigned owner full name. |
| `owner.id` | number | Assigned owner identifier. |
| `paymentTerm.value` | string | Payment term label. |
| `person` | boolean | Whether the record represents a person instead of a company. |
| `primaryAddress.address.city` | string | Primary address city. |
| `primaryAddress.address.country` | string | Primary address country. |
| `primaryAddress.address.countryCode` | string | Primary address country code. |
| `primaryAddress.contactInfo.email` | string | Primary contact email. |
| `primaryAddress.contactInfo.www` | string | Primary website URL. |
| `rating` | string | Assigned company rating. |
| `regNumber` | string | Company registration number. |
| `role` | string | Raynet company role classification. |
| `rowInfo.createdAt` | date | Record creation timestamp. |
| `securityLevel.name` | string | Assigned security level name. |
| `state` | string | Raynet company lifecycle state. |
| `taxNumber` | string | Primary tax number. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET company/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

