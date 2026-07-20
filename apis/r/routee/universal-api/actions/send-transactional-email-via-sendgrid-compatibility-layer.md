# Routee: Send Transactional Email via SendGrid Compatibility Layer

Sends transactional email through Routee's SendGrid compatibility layer.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-transactional-email-via-sendgrid-compatibility-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-transactional-email-via-sendgrid-compatibility-layer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personalizations[].to[]": [
    {}
  ],
  "personalizations[].to[].email": "ava@example.com",
  "personalizations[].cc[].email": "ava@example.com",
  "personalizations[].bcc[].email": "ava@example.com",
  "attachments[].filename": "Ava Chen",
  "attachments[].type": "string",
  "attachments[].content": "string",
  "replyTo.email": "ava@example.com",
  "from": {},
  "from.email": "ava@example.com",
  "content[]": [
    {}
  ],
  "content[].type": "string",
  "content[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-transactional-email-via-sendgrid-compatibility-layer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personalizations[].to[]": [{}],
    "personalizations[].to[].email": "ava@example.com",
    "personalizations[].cc[].email": "ava@example.com",
    "personalizations[].bcc[].email": "ava@example.com",
    "attachments[].filename": "Ava Chen",
    "attachments[].type": "string",
    "attachments[].content": "string",
    "replyTo.email": "ava@example.com",
    "from": {},
    "from.email": "ava@example.com",
    "content[]": [{}],
    "content[].type": "string",
    "content[].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | object | no | You may add up to ten (10) custom headers in format {"customHeader1Name" : "customHeader1Value", "customHeader2Name" : "customHeader2Value" ...} |
| `mailSettings` | object | no | Optional parameter (object) mail_settings contains a child object : footer |
| `mailSettings.footer` | object | no | The object mail_settings.footer contains two properties reflecting the additional text to be included at the end of HTML or Text message bodies. |
| `mailSettings.footer.html` | string | no | The html content of footer (partial HTML). If mail_settings.footer is present, this property must contain a valid partial HTML string. |
| `mailSettings.footer.text` | string | no | If you wish to set a custom footer to be added to plain/text message part of your email, then indicate the string you wish to be appended at the end of your message. |
| `personalizations[]` | array<object> | no | Personalizations array contains arrays of emailAddresses representing contacts to be included in the "to","cc" and "bcc" headers of your message |
| `personalizations[].to[]` | array<object> | yes | The array that indicates the recipients of an actual message. |
| `personalizations[].to[].email` | string | yes | This property holds the actual email address of a recipient. At least one recipient must be indicated in the personalizations.to array to be able to submit a message. |
| `personalizations[].to[].name` | string | no | Optional string indicating the friendly name to be displayed in the messages "to" header (i.e. "John Doe"). |
| `personalizations[].cc[]` | array<object> | no | Optional array of objects indicating recipients to be added to carbon copy of a message. If present, it must contain at least 1 recipient. |
| `personalizations[].cc[].email` | string | yes | If optional personalizations.cc array is present, it must contain at least one recipient with valid email address. This property holds the email address to be included in the "cc" message header. |
| `personalizations[].cc[].name` | string | no | Optional string containing the friendly name of the email address to be added to the carbon copy recipients. |
| `personalizations[].bcc[]` | array<object> | no | Optional array of blind carbon copy recipients. |
| `personalizations[].bcc[].email` | string | yes | If the optional array of BCC recipients is present, then it must contain at least one valid email address. |
| `personalizations[].bcc[].name` | string | no | A friendly name to be used when sending a bcc to the above mentioned email address. |
| `attachments[]` | array<object> | no | Optional array of objects containing the file attachments. |
| `attachments[].filename` | string | yes | A valid file name to be prompted when this attachment is attempted to be saved |
| `attachments[].type` | string | yes | A valid MIME type for the content. Please note that not all types of content are allowed by all providers. Most will disallow any executable file such as .cmd, .vbs etc. |
| `attachments[].content` | string | yes | Base64 encoded content of the attachment file. |
| `replyTo` | object | no | Optional object indicating which will be the address to use in case when the recipient replies to the message. If not set, then the contents of **from** objects are used. |
| `replyTo.name` | string | no | Optional property indicating the friendly name of the return address to be displayed when the recipient replies to a message. |
| `replyTo.email` | string | yes | If the optional reply_to object is present then this property is required. It indicates the actual email address to be used as recipient when a message recipient replies to a message. |
| `subject` | string | no | The subject of the email, up to 144 UTF8 characters. It is not strictly required but it is strongly recommended to fill this property with something meaningful. |
| `from` | object | yes | This is a required object representing the sender of this message. |
| `from.email` | string | yes | This property represents the email address to appear in the "from" message header. |
| `from.name` | string | no | Optional friendly name of the sender. |
| `content[]` | array<object> | yes | Array containing the content of the message divided based on content type (html, text). |
| `content[].type` | string | yes | This property contains the exact MIME type of the content following. Acceptable values are "text/html" and "text/plain". Other MIME types will be rejected. |
| `content[].value` | string | yes | This property encapsulates the actual data to be included in the section, i.e. the actual HTML message body or the Text message body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /transactional-email/sg/` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email-via-sendgrid-compatibility-layer.md) for the provider-specific parameters and requirements.

