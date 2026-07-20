# Sertifier: Add Credentials To Campaign

Adds credentials to a Sertifier campaign.

```
POST https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-credentials-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-credentials-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentials[].campaignId": "Campaign ID",
  "credentials[].name": "Credential recipient name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-credentials-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentials[].campaignId": "Campaign ID",
    "credentials[].name": "Credential recipient name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentials[].campaignId` | string | yes | Example: `Campaign ID`. |
| `credentials[].name` | string | yes | Example: `Credential recipient name`. |
| `credentials[].email` | string | no | Example: `recipient@example.com`. |
| `credentials[].issueDate` | date | no |  |
| `credentials[].expireDate` | date | no |  |
| `credentials[].quickPublish` | boolean | no | Default: `false`. |
| `credentials[].externalId` | string | no | Example: `External entity ID`. |
| `credentials[].dontSendEmail` | boolean | no | Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sertifier API returns.

## Native endpoint

Through the native Sertifier API, this operation is `POST /campaign/addCredentials` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-credentials-to-campaign.md) for the provider-specific parameters and requirements.

