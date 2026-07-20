# Vybit: List All Peeps



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-peeps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-peeps?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-peeps?${params}`, {
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
| `limit` | number | no | Maximum number of peep records to return. |
| `offset` | number | no | Number of peep records to skip. |
| `search` | string | no | Search peeps by name or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "key": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vybKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessStatus` | string | Access state for the subscription relationship. |
| `createdAt` | date | When the peep record was created. |
| `key` | string | Unique peep identifier. |
| `name` | string | Display name of the subscriber. |
| `updatedAt` | date | When the peep record was last updated. |
| `vybKey` | string | Key of the vybit this peep follows. |

## Native endpoint

Through the native Vybit API, this operation is `GET /peeps` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-peeps.md) for the provider-specific parameters and requirements.

