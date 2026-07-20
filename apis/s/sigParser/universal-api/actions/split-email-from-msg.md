# SigParser: Split Email From MSG



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/split-email-from-msg
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/split-email-from-msg?connectionId=$CONNECTION_ID&msgFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msgFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/split-email-from-msg?${params}`, {
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
| `msgFile` | file | yes | Upload the Outlook MSG file contents for the email to split. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanedBodyHtml": "string",
      "CleanedBodyPlain": "string",
      "Date": "string",
      "Emails": [
        {}
      ],
      "EmailTypes": [
        "ava@example.com"
      ],
      "Errors": [
        "string"
      ],
      "FullHtmlBody": "string",
      "FullPlainTextBody": "string",
      "Headers": {},
      "IsSpammyLookingEmailMessage": true,
      "IsSpammyLookingSender": true,
      "MsgType": "string",
      "Subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CleanedBodyHtml` | string | Top email HTML body with signatures and reply chains removed. |
| `CleanedBodyPlain` | string | Top email body with signatures and reply chains removed. |
| `Date` | string | Email date returned by SigParser. |
| `Emails` | array<object> | Email messages extracted from the conversation, newest first. |
| `EmailTypes` | array<string> | Detected email classifications. |
| `Errors` | array<string> | Split or parsing errors returned by SigParser. |
| `FullHtmlBody` | string | Full HTML body. |
| `FullPlainTextBody` | string | Full plain-text body. |
| `Headers` | object | Parsed email headers. |
| `IsSpammyLookingEmailMessage` | boolean | Whether the email body looks spammy or machine-generated. |
| `IsSpammyLookingSender` | boolean | Whether the sender looks spammy. |
| `MsgType` | string | Message type for MSG inputs when available. |
| `Subject` | string | Email subject. |

## Native endpoint

Through the native SigParser API, this operation is `POST /api/Parse/Email/Message/MSG` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-email-from-msg.md) for the provider-specific parameters and requirements.

