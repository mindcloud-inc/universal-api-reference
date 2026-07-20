# Zoho CRM: Convert Lead

Converts a lead into CRM records in Zoho CRM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/convert-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/convert-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "7323083000000731821"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/convert-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "7323083000000731821"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | Lead record ID to convert. Example: `7323083000000731821`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].overwrite` | boolean | no | Overwrite existing mapped values during conversion. |
| `data[].notifyLeadOwner` | boolean | no | Notify the lead owner about the conversion. |
| `data[].notifyNewEntityOwner` | boolean | no | Notify the owner of the newly created record. |
| `data[].moveAttachmentsTo.apiName` | list | no | Module that should receive converted lead attachments. One of: `Accounts`, `Contacts`, `Deals`. Example: `Contacts`. |
| `data[].assignTo.id` | string | no | User ID for the converted record owner. Example: `7323083000000097001`. |
| `data[].accounts.id` | string | no | Existing account ID to associate during conversion. Example: `7323083000000098001`. |
| `data[].contacts.id` | string | no | Existing contact ID to associate during conversion. Example: `7323083000000099001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
        "accounts": {
          "id": "string",
          "name": "Ava Chen"
        },
        "contacts": {
          "id": "string",
          "name": "Ava Chen"
        },
        "deals": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Zoho conversion result code. |
| `details.accounts.id` | string | Converted account record ID. |
| `details.accounts.name` | string | Converted account record name. |
| `details.contacts.id` | string | Converted contact record ID. |
| `details.contacts.name` | string | Converted contact record name. |
| `details.deals.id` | string | Converted deal record ID when a deal is created. |
| `details.deals.name` | string | Converted deal record name when a deal is created. |
| `message` | string | Provider success or failure message. |
| `status` | string | Provider operation status. |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Leads/:record_id/actions/convert` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-lead.md) for the provider-specific parameters and requirements.

