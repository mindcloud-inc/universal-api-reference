# Envoice: Delete Invoice

Deletes an existing invoice from Envoice.

```
DELETE https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-invoice?${params}`, {
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
| `id` | number | yes | Invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number | Deleted invoice identifier. |

## Native endpoint

Through the native Envoice API, this operation is `POST invoice/delete` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice.md) for the provider-specific parameters and requirements.

