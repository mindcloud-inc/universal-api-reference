# HubSpot: List Business Units for User

Retrieves business units for a HubSpot user.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-business-units-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-business-units-for-user?connectionId=$CONNECTION_ID&userId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-business-units-for-user?${params}`, {
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
| `userId` | string | yes | The HubSpot user ID. Example: `123456789`. |
| `name[]` | array<string> | no | A list of business unit names to filter by. Example: `Default Brand`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties[]` | array<string> | no | Optional business unit properties to include. Example: `logoMetadata`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "logoMetadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The business unit ID. |
| `logoMetadata` | object | Business unit logo metadata when requested. |
| `name` | string | The business unit name. |

## Native endpoint

Through the native HubSpot API, this operation is `GET business-units/v3/business-units/user/:userId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-units-for-user.md) for the provider-specific parameters and requirements.

