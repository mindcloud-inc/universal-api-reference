# Zoho CRM: Create Opportunity Group

Creates a new Opportunity Group in Zoho CRM.

```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-opportunity-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-opportunity-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Group A",
  "dealId": "1234567890000000001",
  "totalPrice": "1499.99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-opportunity-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Group A",
    "dealId": "1234567890000000001",
    "totalPrice": "1499.99"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Opportunity Group name. Example: `Group A`. |
| `dealId` | string | yes | Zoho CRM Deal record ID to associate with the Opportunity Group. Example: `1234567890000000001`. |
| `totalPrice` | number | yes | Opportunity Group total price value. Example: `1499.99`. |
| `description` | string | no | Opportunity Group description. Example: `Test group`. |

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
| `code` | string | Zoho CRM create result code. |
| `details.approvalState` | string | Approval state for the created record when returned by Zoho CRM. |
| `details.createdBy.id` | string | ID of the user who created the record. |
| `details.createdBy.name` | string | Name of the user who created the record. |
| `details.createdTime` | date | Created timestamp for the new record. |
| `details.id` | string | Created Opportunity Group record ID. |
| `details.modifiedBy.id` | string | ID of the user who last modified the record. |
| `details.modifiedBy.name` | string | Name of the user who last modified the record. |
| `details.modifiedTime` | date | Last modified timestamp for the created record. |
| `message` | string | Zoho CRM create result message. |
| `status` | string | Zoho CRM create result status. |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Opportunity_Groups` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity-group.md) for the provider-specific parameters and requirements.

