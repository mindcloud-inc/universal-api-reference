# Vapi Universal API Examples

These examples use the MindCloud API key and Vapi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assistants

Retrieves a list of assistants from Vapi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-assistants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-assistants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "analysisPlan": {},
      "artifactPlan": {},
      "backgroundSound": "string",
      "backgroundSpeechDenoisingPlan": {},
      "clientMessages": "string",
      "compliancePlan": {},
      "createdAt": "string",
      "credentialIds": [
        "string"
      ],
      "credentials": [
        {}
      ],
      "endCallMessage": "string",
      "endCallPhrases": [
        "string"
      ],
      "firstMessage": "string",
      "firstMessageInterruptionsEnabled": true,
      "firstMessageMode": "string",
      "hooks": [
        {}
      ],
      "id": "string",
      "keypadInputPlan": {},
      "maxDurationSeconds": 1,
      "metadata": {},
      "model": {},
      "modelOutputInMessagesEnabled": true,
      "monitorPlan": {},
      "name": "Ava Chen",
      "observabilityPlan": {},
      "orgId": "string",
      "server": {},
      "serverMessages": "string",
      "startSpeakingPlan": {},
      "stopSpeakingPlan": {},
      "transcriber": {},
      "transportConfigurations": [
        {}
      ],
      "updatedAt": "string",
      "voice": {},
      "voicemailDetection": {},
      "voicemailMessage": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Assistants action reference](actions/list-assistants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vapi/latest/actions/list-assistants).

## Create Assistant

Creates a new assistant in Vapi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-assistant', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "analysisPlan": {},
      "artifactPlan": {},
      "backgroundSound": "string",
      "backgroundSpeechDenoisingPlan": {},
      "clientMessages": "string",
      "compliancePlan": {},
      "createdAt": "string",
      "credentialIds": [
        "string"
      ],
      "credentials": [
        {}
      ],
      "endCallMessage": "string",
      "endCallPhrases": [
        "string"
      ],
      "firstMessage": "string",
      "firstMessageInterruptionsEnabled": true,
      "firstMessageMode": "string",
      "hooks": [
        {}
      ],
      "id": "string",
      "keypadInputPlan": {},
      "maxDurationSeconds": 1,
      "metadata": {},
      "model": {},
      "modelOutputInMessagesEnabled": true,
      "monitorPlan": {},
      "name": "Ava Chen",
      "observabilityPlan": {},
      "orgId": "string",
      "server": {},
      "serverMessages": "string",
      "startSpeakingPlan": {},
      "stopSpeakingPlan": {},
      "transcriber": {},
      "transportConfigurations": [
        {}
      ],
      "updatedAt": "string",
      "voice": {},
      "voicemailDetection": {},
      "voicemailMessage": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Assistant action reference](actions/create-assistant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vapi/latest/actions/create-assistant).
