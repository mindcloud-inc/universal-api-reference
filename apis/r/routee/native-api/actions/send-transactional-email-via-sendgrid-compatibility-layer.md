# Send Transactional Email via SendGrid Compatibility Layer with Routee

Sends transactional email through Routee's SendGrid compatibility layer.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional-email/sg/`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send Transactional Email via SendGrid Compatibility Layer](https://docs.routee.net/reference/email-v2-sg-compatibility)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers` | body | `object` | no | You may add up to ten (10) custom headers in format {"customHeader1Name" : "customHeader1Value", "customHeader2Name" : "customHeader2Value" ...} |
| `mailSettings` | body | `object` | no | Optional parameter  (object) mail_settings contains a child object : footer |
| `mailSettings.footer` | body | `object` | no | The object mail_settings.footer contains two properties reflecting the additional text to be included at the end of HTML or Text message bodies. |
| `mailSettings.footer.html` | body | `string` | no | The html content of footer (partial HTML). If mail_settings.footer is present, this property must contain a valid partial HTML string. |
| `mailSettings.footer.text` | body | `string` | no | If you wish to set a custom footer to be added to plain/text message part of your email, then indicate the string you wish to be appended at the end of your message. |
| `personalizations[]` | body | `array<object>` | no | Personalizations array contains arrays of emailAddresses representing contacts to be included in the "to","cc" and "bcc" headers of your message |
| `personalizations[].to[]` | body | `array<object>` | yes | The array that indicates the recipients of an actual message. |
| `personalizations[].to[].email` | body | `string` | yes | This property holds the actual email address of a recipient. At least one recipient must be indicated in the personalizations.to array to be able to submit a message. |
| `personalizations[].to[].name` | body | `string` | no | Optional string indicating the friendly name to be displayed in the messages "to" header (i.e. "John Doe"). |
| `personalizations[].cc[]` | body | `array<object>` | no | Optional array of objects indicating recipients to be added to carbon copy of a message. If present, it must contain at least 1 recipient. |
| `personalizations[].cc[].email` | body | `string` | yes | If optional personalizations.cc array is present, it must contain at least one recipient with valid email address. This property holds the email address to be included in the "cc" message header. |
| `personalizations[].cc[].name` | body | `string` | no | Optional string containing the friendly name of the email address to be added to the carbon copy recipients. |
| `personalizations[].bcc[]` | body | `array<object>` | no | Optional array of blind carbon copy recipients. |
| `personalizations[].bcc[].email` | body | `string` | yes | If the optional array of BCC recipients is present, then it must contain at least one valid email address. |
| `personalizations[].bcc[].name` | body | `string` | no | A friendly name to be used when sending a bcc to the above mentioned email address. |
| `attachments[]` | body | `array<object>` | no | Optional array of objects containing the file attachments. |
| `attachments[].filename` | body | `string` | yes | A valid file name to be prompted when this attachment is attempted to be saved |
| `attachments[].type` | body | `string` | yes | A valid MIME type for the content. Please note that not all types of content are allowed by all providers. Most will disallow any executable file such as .cmd, .vbs etc. |
| `attachments[].content` | body | `string` | yes | Base64 encoded content of the attachment file. |
| `replyTo` | body | `object` | no | Optional object indicating which will be the address to use in case when the recipient replies to the message. If not set, then the contents of **from** objects are used. |
| `replyTo.name` | body | `string` | no | Optional property indicating the friendly name of the return address to be displayed when the recipient replies to a message. |
| `replyTo.email` | body | `string` | yes | If the optional reply_to object is present then this property is required. It indicates the actual email address to be used as recipient when a message recipient replies   to a message. |
| `subject` | body | `string` | no | The subject of the email, up to  144 UTF8 characters. It is not strictly required but it is strongly recommended to fill this property with something meaningful. |
| `from` | body | `object` | yes | This is a required object representing the sender of this message. |
| `from.email` | body | `string` | yes | This property represents the email address to appear in the "from" message header. |
| `from.name` | body | `string` | no | Optional friendly name of the sender. |
| `content[]` | body | `array<object>` | yes | Array containing the content of the message divided based on content type (html, text). |
| `content[].type` | body | `string` | yes | This property contains the exact MIME type of the content following. Acceptable values are "text/html" and "text/plain". Other MIME types will be rejected. |
| `content[].value` | body | `string` | yes | This property encapsulates the actual data to be included in the section, i.e. the actual HTML message body or the Text message body. |
