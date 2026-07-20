# Othership: List Users

Retrieves user records from Othership SCIM.

```
GET https://connect.mindcloud.co/v1/universal/othership/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Othership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/othership/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/othership/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | SCIM filter expression used to limit returned users. |
| `sortBy` | string | no | SCIM attribute used to sort returned users. |
| `sortOrder` | string | no | Sort direction for the SCIM list request. |
| `startIndex` | number | no | 1-based start position for paginated SCIM results. |
| `count` | number | no | Maximum number of SCIM results to return. |
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

Through the native Othership API, this operation is `GET /Users` (base URL `https://hwms-api.othership.com/api/v1/azure/scim`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

