# Ringg AI: Upload Campaign Contact List

Uploads a campaign contact list to Ringg AI.

```
POST https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/upload-campaign-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/upload-campaign-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variablesMap": "string",
  "agentId": "string",
  "callConfig": "string",
  "countryCode": "string",
  "campaignStartTime": "string",
  "campaignEndTime": "string",
  "campaignName": "Ava Chen",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/upload-campaign-contact-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variablesMap": "string",
    "agentId": "string",
    "callConfig": "string",
    "countryCode": "string",
    "campaignStartTime": "string",
    "campaignEndTime": "string",
    "campaignName": "Ava Chen",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variablesMap` | string | yes | (Required) JSON string mapping variable names to columns |
| `agentId` | string | yes | (Required) Unique identifier for the agent |
| `callConfig` | string | yes | (Required) JSON string of call configuration |
| `countryCode` | string | yes | (Required) Phone number country code (e.g., +91 for India, +1 for US) |
| `campaignStartTime` | string | yes | (Required) Start time for the campaign (DD/MM/YYYY, HH:MM format) |
| `campaignEndTime` | string | yes | (Required) End time for the campaign (DD/MM/YYYY, HH:MM format) |
| `campaignName` | string | yes | (Required) Name of the campaign. |
| `file` | string | yes | (Required) CSV file containing the contact list. |
| `removeInvalidRows` | boolean | no | (Optional) Auto-remove invalid rows from CSV |
| `transliterateCalleeName` | boolean | no | (Optional) Transliterate callee names to the agent's language |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customArgsValues": [
        {}
      ],
      "failedRows": 1,
      "listId": "string",
      "message": "string",
      "successfulRows": 1,
      "totalRows": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customArgsValues` | array<object> | Array of custom variables for each contact |
| `failedRows` | number | Number of rows that failed validation |
| `listId` | string | ID of the created campaign list |
| `message` | string |  |
| `successfulRows` | number | Number of successfully processed rows |
| `totalRows` | number | Total number of rows in uploaded CSV |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /campaign/save` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-campaign-contact-list.md) for the provider-specific parameters and requirements.

