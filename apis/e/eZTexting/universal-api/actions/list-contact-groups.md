# EZ Texting: List Contact Groups

Retrieves contact groups from EZ Texting.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contact-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contact-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contact-groups?${params}`, {
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
| `filters[name][like]` | string | no | Filter contact groups by name |
| `page` | number | no | Page offset starting at 0 |
| `size` | number | no | Page size |
| `sort` | string | no | Sort field and direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "id": "string",
      "name": "Ava Chen",
      "note": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `GET /contact-groups` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-groups.md) for the provider-specific parameters and requirements.

