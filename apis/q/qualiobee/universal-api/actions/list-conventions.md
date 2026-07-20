# Qualiobee: List Conventions

Retrieves conventions from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-conventions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-conventions?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-conventions?${params}`, {
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
| `organizationUuid` | string | yes |  |
| `withDeleted` | boolean | no | Default: `false`. |
| `relations` | list<string> | no | Accepts multiple values as an array. |
| `uuid` | string | no |  |
| `isDisabled` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customer": {},
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "isDisabled": true,
      "isSigned": true,
      "pricing": {},
      "session": {},
      "updateDate": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | The date when the convention was created |
| `customer` | object | The customer linked to the convention when requested |
| `deleteDate` | date | The date when the convention was deleted |
| `isDisabled` | boolean | Whether the convention file is disabled for the customer in the learning session or not |
| `isSigned` | boolean | Whether the convention file is signed or not |
| `pricing` | object | The pricing details linked to the convention when requested |
| `session` | object | The learning session linked to the convention when requested |
| `updateDate` | date | The last date when the convention was updated |
| `uuid` | string | The uuid of the convention |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/convention` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conventions.md) for the provider-specific parameters and requirements.

