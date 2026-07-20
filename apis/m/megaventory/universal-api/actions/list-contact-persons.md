# Megaventory: List Contact Persons

Retrieves contact person records from Megaventory.

```
GET https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-contact-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-contact-persons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-contact-persons?${params}`, {
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
| `Filters` | list<object> | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | number | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | boolean | no | Include archived contact person records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mvContactPersons": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mvContactPersons` | array<object> |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/ContactPersonGet` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-persons.md) for the provider-specific parameters and requirements.

