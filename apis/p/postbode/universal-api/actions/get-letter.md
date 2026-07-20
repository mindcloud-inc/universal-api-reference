# Postbode: Get Letter

Retrieves a letter from a specific Postbode mailbox.

```
GET https://connect.mindcloud.co/v1/universal/postbode/latest/actions/get-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postbode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/get-letter?connectionId=$CONNECTION_ID&mailboxId=155198&letterId=2486674" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailboxId": "155198",
  "letterId": "2486674"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postbode/latest/actions/get-letter?${params}`, {
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
| `mailboxId` | number | yes | The Postbode mailbox ID. Example: `155198`. |
| `letterId` | number | yes | The Postbode letter ID. Example: `2486674`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "content": "string",
      "documents": [
        {}
      ],
      "envelope_id": 1,
      "formatted_id": "string",
      "id": 1,
      "mailbox_id": 1,
      "metadata": {},
      "pages": 1,
      "pdf": "string",
      "pricing": {},
      "printing": "string",
      "retour_envelope_id": 1,
      "retour_scan": "string",
      "service": "string",
      "sheets": 1,
      "shipping_id": 1,
      "shipping_method_id": 1,
      "status": "string",
      "tracking_code": "string",
      "uuid": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `content` | string |  |
| `documents` | array<object> |  |
| `envelope_id` | number |  |
| `formatted_id` | string |  |
| `id` | number |  |
| `mailbox_id` | number |  |
| `metadata` | object |  |
| `pages` | number |  |
| `pdf` | string |  |
| `pricing` | object |  |
| `printing` | string |  |
| `retour_envelope_id` | number |  |
| `retour_scan` | string |  |
| `service` | string |  |
| `sheets` | number |  |
| `shipping_id` | number |  |
| `shipping_method_id` | number |  |
| `status` | string |  |
| `tracking_code` | string |  |
| `uuid` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native Postbode API, this operation is `GET /mailbox/:mailbox_id/letter/:letter_id` (base URL `https://app.postbode.nu/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-letter.md) for the provider-specific parameters and requirements.

