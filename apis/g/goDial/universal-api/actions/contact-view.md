# GoDial: Get Contact

Retrieves details for a contact from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/contact-view?${params}`, {
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
| `id` | string | yes | Contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dispo": "string",
      "email": "ava@example.com",
      "id": "string",
      "listId": "string",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `dispo` | string |  |
| `email` | string |  |
| `id` | string |  |
| `listId` | string |  |
| `name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/contact/[:id]/view` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contact-view.md) for the provider-specific parameters and requirements.

