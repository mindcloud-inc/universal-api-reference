# Zoho CRM: Upsert Account

Finds an account in Zoho CRM, or creates one if needed.

```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].accountName": "MindCloud Wizard Account 20260311 2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].accountName": "MindCloud Wizard Account 20260311 2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Account records to upsert. |
| `data[].accountName` | string | yes | Example: `MindCloud Wizard Account 20260311 2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
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
      "duplicateField": "string",
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
| `action` | string |  |
| `code` | string |  |
| `details.approvalState` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `duplicateField` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Accounts/upsert` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-account.md) for the provider-specific parameters and requirements.

