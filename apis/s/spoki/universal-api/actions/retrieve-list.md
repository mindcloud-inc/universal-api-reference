# Spoki: Retrieve List

Retrieves a contact list by ID.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-list?${params}`, {
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
| `id` | number | yes | The list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "contactsCount": 1,
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `contactsCount` | number |  |
| `createdDatetime` | date |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Spoki API, this operation is `GET /lists/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-list.md) for the provider-specific parameters and requirements.

