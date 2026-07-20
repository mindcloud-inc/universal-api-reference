# Create Campaign with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign.create/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Create Campaign](https://chmyos.notion.site/Create-a-Campaign-v2-0-937e18e29f374c7da5233e1762f81526)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Name of your campaign |
| `FromName` | body | `string` | yes | The name shown in the from email header |
| `FromEmail` | body | `string` | yes | Sender email address |
| `ReplyToName` | body | `string` | yes | The name shown in the reply-to header |
| `ReplyToEmail` | body | `string` | yes | Email address to receive replies |
| `Recipients` | body | `string` | yes | ID numbers of recipient lists |
| `Subject` | body | `string` | yes | Subject of your email campaign |
| `PlainContent` | body | `string` | no | Text content of your email campaign |
| `HTMLContent` | body | `string` | yes | HTML content of your email campaign |
