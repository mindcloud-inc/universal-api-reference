# ProvenExpert: Create Invitation Mail

Creates and sends survey invitation emails in ProvenExpert.

```
POST https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.code": "VRTQ13",
  "data.recipients[]": [
    {}
  ],
  "data.recipients[].email": "reviewer@example.org"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.code": "VRTQ13",
    "data.recipients[]": [{}],
    "data.recipients[].email": "reviewer@example.org"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.code` | string | yes | Survey code for which invitation emails should be created. Example: `VRTQ13`. |
| `data.reminder` | number | no | Whether ProvenExpert should send a reminder email after 7 days. Provider default is 1 when omitted. Example: `1`. |
| `data.recipients[]` | array<object> | yes | Recipient list for the invitation mailing. |
| `data.recipients[].email` | string | yes | Email address of the recipient. Example: `reviewer@example.org`. |
| `data.recipients[].name` | string | no | Name of the recipient. Example: `John Doe`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.recipients[].subject` | string | no | Custom email subject for the invitation email. Example: `Your opinion is requested: Give me feedback!`. |
| `data.recipients[].salutation` | string | no | Custom salutation in the invitation email. Example: `Dear Mr. Doe`. |
| `data.recipients[].text` | string | no | Custom invitation email body text. Example: `Thanks for the interesting consultation yesterday. To rate the consulting services, you can use the following link:`. |
| `data.recipients[].reminderSubject` | string | no | Custom subject for the reminder email. Example: `Reminder: Your opinion is requested: Give me feedback!`. |
| `data.recipients[].reminderSalutation` | string | no | Custom salutation in the reminder email. Example: `Dear Mr. Doe`. |
| `data.recipients[].reminderText` | string | no | Custom reminder email body text. Example: `Last week we had the consultation. If you want to evaluate the consulting services, you can click the following link:`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": {
        "all": 1,
        "created": 1,
        "error": 1,
        "inviteExists": 1,
        "ratingExists": 1
      },
      "id": "string",
      "list": {
        "created": [
          "string"
        ],
        "error": [
          "string"
        ],
        "inviteExists": [
          "string"
        ],
        "ratingExists": [
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
| `count.all` | number | Total recipients included in the mailing request. |
| `count.created` | number | Number of invitation emails created successfully. |
| `count.error` | number | Number of recipients for which the invitation could not be created. |
| `count.inviteExists` | number | Number of recipients for which an invitation already exists. |
| `count.ratingExists` | number | Number of recipients for which a rating already exists. |
| `id` | string | Mailing ID that can be used to query invitation mail status. |
| `list.created` | array<string> | Email addresses for which an invitation was created. |
| `list.error` | array<string> | Email addresses for which invitation creation failed. |
| `list.inviteExists` | array<string> | Email addresses for which an invitation already exists. |
| `list.ratingExists` | array<string> | Email addresses for which a rating already exists. |
| `status` | string | Mailing creation status returned by ProvenExpert. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /invite/mail/create` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invitation-mail.md) for the provider-specific parameters and requirements.

