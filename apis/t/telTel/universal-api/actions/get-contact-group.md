# TelTel: Get Contact Group

Retrieves a contact group from TelTel.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-contact-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-contact-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /contacts/groups/{id}` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-group.md) for the provider-specific parameters and requirements.

