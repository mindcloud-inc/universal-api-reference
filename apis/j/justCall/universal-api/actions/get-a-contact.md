# JustCall: Get a Contact

Retrieves a contact from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-contact?${params}`, {
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
| `id` | number | yes | The JustCall contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/contacts/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-contact.md) for the provider-specific parameters and requirements.

