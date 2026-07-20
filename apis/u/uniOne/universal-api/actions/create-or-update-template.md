# UniOne: Create Or Update Template

Creates or updates an email template in UniOne.

```
POST https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template.name": "Wizard Template 2026-04-02",
  "template.editorType": "html",
  "template.templateEngine": "velocity",
  "template.body.html": "<p>Hello from MindCloud</p>",
  "template.subject": "MindCloud Template Test",
  "template.fromEmail": "no-reply@example.com",
  "template.fromName": "MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template.name": "Wizard Template 2026-04-02",
    "template.editorType": "html",
    "template.templateEngine": "velocity",
    "template.body.html": "<p>Hello from MindCloud</p>",
    "template.subject": "MindCloud Template Test",
    "template.fromEmail": "no-reply@example.com",
    "template.fromName": "MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template.id` | string | no | Template identifier. Reuse the same value to update an existing template. Example: `5f1b6cb0-bc95-4a44-9c77-5d0b8f09c5a1`. |
| `template.name` | string | yes | Template display name. Example: `Wizard Template 2026-04-02`. |
| `template.editorType` | string | yes | Template editor type. Default: `html`. Example: `html`. |
| `template.templateEngine` | string | yes | Template engine used for substitutions. Default: `velocity`. Example: `velocity`. |
| `template.body.html` | string | yes | HTML content of the template body. Example: `<p>Hello from MindCloud</p>`. |
| `template.body.plaintext` | string | no | Plaintext fallback content for the template body. Example: `Hello from MindCloud`. |
| `template.subject` | string | yes | Template subject line. Example: `MindCloud Template Test`. |
| `template.fromEmail` | string | yes | Sender email stored on the template. Example: `no-reply@example.com`. |
| `template.fromName` | string | yes | Sender name stored on the template. Example: `MindCloud`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST template/set.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-template.md) for the provider-specific parameters and requirements.

