# Clockify: Update User Custom Field

Updates a user custom field value in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "customFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "customFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `customFieldId` | string<string> | yes |  |
| `value` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId": "string",
      "customFieldName": "Ava Chen",
      "customFieldType": "string",
      "userId": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId` | string |  |
| `customFieldName` | string |  |
| `customFieldType` | string |  |
| `userId` | string |  |
| `value` | object |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/users/:userId/custom-field/:customFieldId/value` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-custom-field.md) for the provider-specific parameters and requirements.

