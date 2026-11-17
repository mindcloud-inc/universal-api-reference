# ECI Bolt: List Communities



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-communities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-communities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-communities?${params}`, {
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
| `refreshToken` | string | no | Token used to get the changed communities, returned on the last page of the communities. You should only send the refresh_token or the next_batch. |
| `refresh` | string | no | Return only directly changed records when value is "self" |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "city": "string",
      "customer": "string",
      "emailConfirmationToSupervisor": true,
      "etag": "string",
      "externalId": "string",
      "id": 1,
      "mapLocation": "string",
      "name": "Ava Chen",
      "office": "string",
      "projectManager": "string",
      "security": true,
      "shortDescription": "string",
      "supervisor": "string",
      "underWarranty": true,
      "warranties": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `city` | string |  |
| `customer` | string |  |
| `emailConfirmationToSupervisor` | boolean |  |
| `etag` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `mapLocation` | string |  |
| `name` | string |  |
| `office` | string |  |
| `projectManager` | string |  |
| `security` | boolean |  |
| `shortDescription` | string |  |
| `supervisor` | string |  |
| `underWarranty` | boolean |  |
| `warranties` | string |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/communities` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-communities.md) for the provider-specific parameters and requirements.

