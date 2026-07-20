# Othership: Update User

Updates an existing user in Othership.

```
PUT https://connect.mindcloud.co/v1/universal/othership/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Othership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/othership/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/othership/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The SCIM user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "displayName": "Ava Chen",
      "emails": [
        {
          "value": "ava@example.com"
        }
      ],
      "externalId": "string",
      "id": "string",
      "meta": {
        "resourceType": "string"
      },
      "name": {
        "familyName": "Ava Chen",
        "givenName": "Ava Chen"
      },
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `displayName` | string |  |
| `emails[].value` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `meta.resourceType` | string |  |
| `name.familyName` | string |  |
| `name.givenName` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Othership API, this operation is `PATCH /Users/:id` (base URL `https://hwms-api.othership.com/api/v1/azure/scim`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

