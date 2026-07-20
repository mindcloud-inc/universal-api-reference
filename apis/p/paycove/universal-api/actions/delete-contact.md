# Paycove: Delete Contact

Deletes a contact from Paycove.

```
DELETE https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-contact?${params}`, {
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
| `id` | string | yes | Paycove CRMContact ID. Example: `1`. |
| `deleteSubscriptions` | boolean | no | Delete subscriptions associated with this contact. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "successMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `successMsg` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `DELETE contacts/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

