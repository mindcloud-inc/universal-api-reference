# Notifyre SMS: Get Fax Document Status

Retrieves fax document status from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-fax-document-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-fax-document-status?connectionId=$CONNECTION_ID&fileName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-fax-document-status?${params}`, {
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
| `fileName` | string | yes | Converted document file name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string | Converted file name. |
| `id` | string | Converted document identifier. |
| `status` | string | Current conversion status. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /fax/send/conversion/:fileName` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fax-document-status.md) for the provider-specific parameters and requirements.

