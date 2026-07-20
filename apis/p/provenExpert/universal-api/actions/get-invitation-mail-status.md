# ProvenExpert: Get Invitation Mail Status

Retrieves the status of an invitation mailing in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-invitation-mail-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-invitation-mail-status?connectionId=$CONNECTION_ID&data.id=9959c18c32976a5453e704c0c6b28be5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.id": "9959c18c32976a5453e704c0c6b28be5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-invitation-mail-status?${params}`, {
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
| `data.id` | string | yes | ID of the invitation mailing returned by Create Invitation Mail. Example: `9959c18c32976a5453e704c0c6b28be5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": {
        "all": 1,
        "error": 1,
        "pending": 1,
        "sent": 1
      },
      "created": 1,
      "list": {
        "error": [
          "string"
        ],
        "pending": [
          "string"
        ],
        "sent": [
          "string"
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count.all` | number | Total recipients in the mailing. |
| `count.error` | number | Number of emails that could not be sent. |
| `count.pending` | number | Number of emails still pending delivery. |
| `count.sent` | number | Number of emails already sent. |
| `created` | number | Unix timestamp for when the mailing was created. |
| `list.error` | array<string> | Recipients whose emails failed to send. |
| `list.pending` | array<string> | Recipients whose emails are still pending delivery. |
| `list.sent` | array<string> | Recipients whose emails were already sent. |
| `status` | string | Current mailing delivery status returned by ProvenExpert. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /invite/mail/status` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invitation-mail-status.md) for the provider-specific parameters and requirements.

