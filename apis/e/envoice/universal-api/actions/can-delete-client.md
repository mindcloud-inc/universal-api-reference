# Envoice: Can Delete Client

Checks whether a client can be deleted in Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/can-delete-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/can-delete-client?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/can-delete-client?${params}`, {
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
| `id` | number | yes | Client identifier to check for deletion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CanDelete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CanDelete` | boolean | Whether the client can be deleted. |

## Native endpoint

Through the native Envoice API, this operation is `GET client/candelete` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/can-delete-client.md) for the provider-specific parameters and requirements.

