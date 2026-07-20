# AeroLeads: Get Company Email



```
GET https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AeroLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email?connectionId=$CONNECTION_ID&firstName=John&lastName=Doe&company=Acme%20Inc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "John",
  "lastName": "Doe",
  "company": "Acme Inc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email?${params}`, {
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
| `firstName` | string | yes | Prospect first name. Example: `John`. |
| `lastName` | string | yes | Prospect last name. Example: `Doe`. |
| `company` | string | yes | Prospect company name. Example: `Acme Inc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AeroLeads API returns.

## Native endpoint

Through the native AeroLeads API, this operation is `GET /api/get_email_details` (base URL `https://aeroleads.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-email.md) for the provider-specific parameters and requirements.

