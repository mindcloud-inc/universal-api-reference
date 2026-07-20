# Zoho CRM: Update Opportunity Group



```
PUT https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-opportunity-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-opportunity-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "7192380000004399806"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-opportunity-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "7192380000004399806"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Zoho CRM Opportunity Group record ID to update. Example: `7192380000004399806`. |
| `name` | string | no | Opportunity Group name. Example: `Group A`. |
| `dealId` | string | no | Zoho CRM Deal record ID to associate with the Opportunity Group. Example: `7192380000004398751`. |
| `totalPrice` | number | no | Opportunity Group total price value. Example: `1499.99`. |
| `description` | string | no | Opportunity Group description. Example: `Updated group`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
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
| `code` | string | Zoho CRM update result code. |
| `details.createdBy.id` | string | ID of the user who created the record. |
| `details.createdBy.name` | string | Name of the user who created the record. |
| `details.createdTime` | date | Created timestamp for the record. |
| `details.id` | string | Updated Opportunity Group record ID. |
| `details.modifiedBy.id` | string | ID of the user who last modified the record. |
| `details.modifiedBy.name` | string | Name of the user who last modified the record. |
| `details.modifiedTime` | date | Last modified timestamp for the updated record. |
| `message` | string | Zoho CRM update result message. |
| `status` | string | Zoho CRM update result status. |

## Native endpoint

Through the native Zoho CRM API, this operation is `PUT /Opportunity_Groups` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-opportunity-group.md) for the provider-specific parameters and requirements.

