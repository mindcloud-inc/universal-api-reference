# Othership: Get User

Retrieves a specific user from Othership.

```
GET https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Othership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The SCIM user identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | string | no | Comma-separated SCIM attributes to include in the response. |
| `excludedAttributes` | string | no | Comma-separated SCIM attributes to omit from the response. |

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

Through the native Othership API, this operation is `GET /Users/:id` (base URL `https://hwms-api.othership.com/api/v1/azure/scim`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

