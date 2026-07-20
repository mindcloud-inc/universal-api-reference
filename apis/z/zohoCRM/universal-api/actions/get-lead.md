# Zoho CRM: Get Lead

Retrieves a lead record from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-lead?connectionId=$CONNECTION_ID&ids=string&fields=id%2CCompany%2CFull_Name%2CEmail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string",
  "fields": "id,Company,Full_Name,Email"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-lead?${params}`, {
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
| `ids` | string | yes | The Zoho CRM record ID to retrieve. |
| `fields` | string | yes | Comma-separated Zoho CRM field API names to include in the response. Default: `id,Company,Full_Name,Email`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Leads` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

