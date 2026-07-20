# HubSpot: Get User

Retrieves a user from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The ID of the user to retrieve. Example: `12345`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProperty` | list | no | Which unique user identifier the `userId` value represents. One of: `hs_email`, `hs_internal_user_id`. |
| `properties` | string | no | Comma-separated list of properties to return. Accepts multiple values in one string, delimited by `,`. Example: `firstname,lastname`. |
| `propertiesWithHistory` | string | no | Comma-separated list of properties to return with value history. Accepts multiple values in one string, delimited by `,`. Example: `firstname`. |
| `associations` | string | no | Comma-separated list of object associations to retrieve with the user. Accepts multiple values in one string, delimited by `,`. Example: `companies,deals`. |
| `archived` | boolean | no | Whether to return archived records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the user record is archived. |
| `createdAt` | date | When the user record was created. |
| `id` | string | The CRM user record ID. |
| `properties` | object | The returned user properties. |
| `updatedAt` | date | When the user record was last updated. |
| `url` | string | The HubSpot settings URL for the user. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/users/:userId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

