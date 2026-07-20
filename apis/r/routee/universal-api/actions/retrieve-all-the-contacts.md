# Routee: Retrieve all the contacts

Retrieves all the contacts from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-contacts?${params}`, {
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
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve, default value is 20. Max value: 2000 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].blacklistedServices[]` | array |  |
| `content[].country` | string |  |
| `content[].firstName` | string |  |
| `content[].groups[]` | array<string> |  |
| `content[].id` | string |  |
| `content[].labels[]` | array |  |
| `content[].lastName` | string |  |
| `content[].mobile` | string |  |
| `content[].vip` | boolean |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /contacts/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-all-the-contacts.md) for the provider-specific parameters and requirements.

