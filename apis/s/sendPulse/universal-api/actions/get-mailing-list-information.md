# SendPulse: Get Mailing List Information

Retrieves a mailing list from SendPulse by ID.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-information?connectionId=$CONNECTION_ID&mailingListId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-information?${params}`, {
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
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_email_qty": 1,
      "active_phones_quantity": 1,
      "all_email_qty": 1,
      "creationdate": "string",
      "exc_phones_quantity": 1,
      "id": 1,
      "inactive_email_qty": 1,
      "name": "Ava Chen",
      "new_phones_quantity": 1,
      "status": 1,
      "status_explain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_email_qty` | number |  |
| `active_phones_quantity` | number |  |
| `all_email_qty` | number |  |
| `creationdate` | string |  |
| `exc_phones_quantity` | number |  |
| `id` | number |  |
| `inactive_email_qty` | number |  |
| `name` | string |  |
| `new_phones_quantity` | number |  |
| `status` | number |  |
| `status_explain` | string |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /addressbooks/:mailingListId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mailing-list-information.md) for the provider-specific parameters and requirements.

