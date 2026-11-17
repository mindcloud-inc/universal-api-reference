# Zoho CRM: Create Custom Object Record



```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-custom-object-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-custom-object-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-custom-object-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | list<string> | yes | Select the exact Zoho API name. Discovery includes standard modules too; custom modules have generatedType=custom. |
| `data[]` | array<object> | yes | One record object using exact Zoho field API names. Include all mandatory module and layout fields. Custom fields are accepted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trigger[]` | array<string> | no | Optional Zoho automation names. Supply an empty array to suppress workflow triggers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
        "$approvalState": "string",
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "string",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "string"
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
| `details` | object |  |
| `details.$approvalState` | string |  |
| `details.createdBy` | object |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | string |  |
| `details.id` | string |  |
| `details.modifiedBy` | object |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /:moduleApiName` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-object-record.md) for the provider-specific parameters and requirements.

