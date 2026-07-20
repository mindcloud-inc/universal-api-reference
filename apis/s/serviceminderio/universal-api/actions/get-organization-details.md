# serviceminder.io: Get Organization Details

Retrieves organization details from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-organization-details?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-organization-details?${params}`, {
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
| `organizationId` | number | yes | Organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "internalName": "Ava Chen",
      "locationId": "string",
      "message": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "resultCode": 1,
      "serviceAgents": [
        {}
      ],
      "services": [
        {}
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `internalName` | string |  |
| `locationId` | string |  |
| `message` | string |  |
| `name` | string |  |
| `organizationId` | number |  |
| `resultCode` | number |  |
| `serviceAgents` | array<object> |  |
| `services` | array<object> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /organizations/details` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

