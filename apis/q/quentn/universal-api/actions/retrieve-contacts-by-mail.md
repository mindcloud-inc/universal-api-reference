# Quentn: Retrieve Contacts by Mail



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contacts-by-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contacts-by-mail?connectionId=$CONNECTION_ID&contact_mail=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_mail": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contacts-by-mail?${params}`, {
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
| `contact_mail` | string | yes | The contact email address to look up in Quentn. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /contact/:contact_mail` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contacts-by-mail.md) for the provider-specific parameters and requirements.

