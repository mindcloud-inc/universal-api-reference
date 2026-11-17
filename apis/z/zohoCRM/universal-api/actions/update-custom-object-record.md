# Zoho CRM: Update Custom Object Record



```
PUT https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-custom-object-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-custom-object-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-custom-object-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string",
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
| `recordId` | string | yes |  |
| `data[]` | array<object> | yes | One record object using exact Zoho field API names. Include all mandatory module and layout fields. Custom fields are accepted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trigger[]` | array<string> | no | Optional Zoho automation names. Supply an empty array to suppress workflow triggers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho CRM API returns.

## Native endpoint

Through the native Zoho CRM API, this operation is `PUT /:moduleApiName/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-object-record.md) for the provider-specific parameters and requirements.

