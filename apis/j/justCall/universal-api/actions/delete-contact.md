# JustCall: Delete Contact

Deletes an existing contact from JustCall.

```
DELETE https://connect.mindcloud.co/v1/universal/justCall/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/delete-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/delete-contact?${params}`, {
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
| `id` | number | no | The JustCall contact ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `DELETE /v2.1/contacts` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

