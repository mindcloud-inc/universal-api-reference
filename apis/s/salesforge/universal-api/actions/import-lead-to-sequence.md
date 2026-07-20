# Salesforge: Import Lead To Sequence

Imports a lead to a sequence in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/import-lead-to-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/import-lead-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes",
  "firstName": "Ada"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/import-lead-to-sequence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "sequenceID": "seq_q266pc1d33ozbe3et0mes",
    "firstName": "Ada"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to import the lead into. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `firstName` | string | yes | Lead first name. Example: `Ada`. |
| `lastName` | string | no | Lead last name. Example: `Lovelace`. |
| `email` | string | no | Lead email address. Example: `ada@example.com`. |
| `company` | string | no | Lead company name. Example: `MindCloud`. |
| `position` | string | no | Lead job title. Example: `Founder`. |
| `linkedinUrl` | string | no | Lead LinkedIn profile URL. Example: `https://linkedin.com/in/ada-lovelace`. |
| `tags[]` | array<string> | no | Tags to apply to the lead. Example: `beta,launch`. |
| `tagIds[]` | array<string> | no | Existing tag IDs to apply to the lead. Example: `tag_123456`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/import-lead` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-lead-to-sequence.md) for the provider-specific parameters and requirements.

