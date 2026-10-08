# Fleetworthy: Search People



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-people?${params}`, {
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
| `stringSearch` | string | no | Search by a person's identifying text. |
| `entitySearch[]` | array<string> | no | Limit the search to Fleetworthy location IDs. |
| `isActive` | boolean | no | Return active people when enabled. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advancedFilter` | object | no | Optional Fleetworthy person filter object, such as firstName, lastName, email, or SocialSecurityNumberLastFour. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isActive": true,
      "lastName": "Chen",
      "needsAttention": true,
      "personNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayId` | string | Fleetworthy person display identifier. |
| `email` | string | Person email address. |
| `firstName` | string | Person first name. |
| `id` | string | Fleetworthy person identifier. |
| `isActive` | boolean | Whether the person is active. |
| `lastName` | string | Person last name. |
| `needsAttention` | boolean | Whether the person needs compliance attention. |
| `personNumber` | string | Fleetworthy person number. |

## Native endpoint

Through the native Fleetworthy API, this operation is `POST /people-bulk/search` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

