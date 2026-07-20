# Alto: Get All Contacts

Retrieves all contact records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-all-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-all-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-all-contacts?${params}`, {
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
| `active` | boolean | no | Whether to return active contacts. |
| `category` | string | no | Contact category filter. |
| `persona` | string | no | Contact persona filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `contactType` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `modifiedAt` | date |  |
| `position` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /contacts/all` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-contacts.md) for the provider-specific parameters and requirements.

