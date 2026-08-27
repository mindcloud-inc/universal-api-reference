# Zoho CRM: Create Account

Creates a new account in Zoho CRM.

```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].accountName": "MindCloud Wizard Account 20260311 1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].accountName": "MindCloud Wizard Account 20260311 1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Account records to create. |
| `data[].A2ZAccountID` | string | no |  |
| `data[].accountName` | string | yes | Example: `MindCloud Wizard Account 20260311 1`. |
| `data[].Shipping_Street` | string | no |  |
| `data[].Shipping_Street_2` | string | no |  |
| `data[].Shipping_City` | string | no |  |
| `data[].Shipping_State` | string | no |  |
| `data[].Shipping_Postcode` | string | no |  |
| `data[].Website` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
        "approvalState": "string",
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "2026-05-07T12:00:00.000Z"
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
| `code` | string |  |
| `details.approvalState` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Accounts` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

