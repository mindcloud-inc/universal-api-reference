# Maildrip: Get contacts in a specific group or all contacts



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contacts-in-a-specific-group-or-all-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contacts-in-a-specific-group-or-all-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contacts-in-a-specific-group-or-all-contacts?${params}`, {
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
| `limit` | string | no |  |
| `page` | number | no |  |
| `search` | string | no |  |
| `groupId` | string | no |  |
| `attributeFilters` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/contacts/group` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contacts-in-a-specific-group-or-all-contacts.md) for the provider-specific parameters and requirements.

