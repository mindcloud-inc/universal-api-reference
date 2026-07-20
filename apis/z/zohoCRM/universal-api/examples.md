# Zoho CRM Universal API Examples

These examples use the MindCloud API key and Zoho CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves an account record from Zoho CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-account?connectionId=$CONNECTION_ID&ids=string&fields=id%2CAccount_Name%2CPhone%2CWebsite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string",
  "fields": "id,Account_Name,Phone,Website"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-account?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "id": "string",
      "phone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCRM/latest/actions/get-account).

## Convert Lead

Converts a lead into CRM records in Zoho CRM.

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

Example response:

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

See the full [Convert Lead action reference](actions/convert-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCRM/latest/actions/convert-lead).
