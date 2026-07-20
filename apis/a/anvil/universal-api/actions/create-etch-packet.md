# Anvil: Create Etch Packet

Creates a new Etch packet in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-etch-packet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-etch-packet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-etch-packet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.name` | string | no | Provide Name for Create Etch Packet. |
| `variables.organizationEid` | string | no | Provide Organization EID for Create Etch Packet. |
| `variables.isDraft` | boolean | no | Provide Is Draft for Create Etch Packet. |
| `variables.isTest` | boolean | no | Provide Is Test for Create Etch Packet. |
| `variables.files[]` | array<object> | no | Provide Files for Create Etch Packet. |
| `variables.signers[]` | array<object> | no | Provide Signers for Create Etch Packet. |
| `variables.signatureRecipients[]` | array<object> | no | Provide Signature Recipients for Create Etch Packet. |
| `variables.data` | object | no | Provide Data for Create Etch Packet. |
| `variables.replyToName` | string | no | Provide Reply To Name for Create Etch Packet. |
| `variables.replyToEmail` | string | no | Provide Reply To Email for Create Etch Packet. |
| `variables.signatureEmailSubject` | string | no | Provide Signature Email Subject for Create Etch Packet. |
| `variables.signatureEmailBody` | string | no | Provide Signature Email Body for Create Etch Packet. |
| `variables.signaturePageOptions` | object | no | Provide Signature Page Options for Create Etch Packet. |
| `variables.finishPageOptions` | object | no | Provide Finish Page Options for Create Etch Packet. |
| `variables.enableEmails` | object | no | Provide Enable Emails for Create Etch Packet. |
| `variables.createCastTemplatesFromUploads` | boolean | no | Provide Create Cast Templates From Uploads for Create Etch Packet. |
| `variables.duplicateCasts` | boolean | no | Provide Duplicate Casts for Create Etch Packet. |
| `variables.mergePDFs` | boolean | no | Provide Merge PDFs for Create Etch Packet. |
| `variables.allowUpdates` | boolean | no | Provide Allow Updates for Create Etch Packet. |
| `variables.webhookURL` | string | no | Provide Webhook URL for Create Etch Packet. |
| `variables.signatureProvider` | string | no | Provide Signature Provider for Create Etch Packet. |
| `variables.advancedCreate` | boolean | no | Provide Advanced Create for Create Etch Packet. |
| `variables.detectBoxesAdvanced` | boolean | no | Provide Detect Boxes Advanced for Create Etch Packet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-etch-packet.md) for the provider-specific parameters and requirements.

