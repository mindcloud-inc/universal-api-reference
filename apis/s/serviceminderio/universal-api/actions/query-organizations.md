# serviceminder.io: Query Organizations

Finds organizations in ServiceMinder by name.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-organizations?${params}`, {
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
| `nameSearch` | string | no | Search organizations by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "includeInactive": true,
      "internalName": "Ava Chen",
      "locationId": "string",
      "message": "string",
      "organizations": [
        {}
      ],
      "postalCode": "string",
      "publicName": "Ava Chen",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `includeInactive` | boolean |  |
| `internalName` | string |  |
| `locationId` | string |  |
| `message` | string |  |
| `organizations` | array<object> |  |
| `postalCode` | string |  |
| `publicName` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /organizations/query` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-organizations.md) for the provider-specific parameters and requirements.

