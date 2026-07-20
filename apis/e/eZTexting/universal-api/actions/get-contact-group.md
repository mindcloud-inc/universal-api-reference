# EZ Texting: Get Contact Group

Retrieves a contact group from EZ Texting.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact-group?${params}`, {
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
| `id` | string | yes | Contact group ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "id": "string",
      "name": "Ava Chen"
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

## Native endpoint

Through the native EZ Texting API, this operation is `GET /contact-groups/:id` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-group.md) for the provider-specific parameters and requirements.

