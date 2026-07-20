# UpGuard Universal API Examples

These examples use the MindCloud API key and UpGuard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Risks

Retrieves available risk definitions from the UpGuard platform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-available-risks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-available-risks?${params}`, {
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
      "category": "string",
      "description": "string",
      "finding": "string",
      "generic": true,
      "group": "string",
      "id": "string",
      "remediation": "string",
      "risk": "string",
      "riskDetails": "string",
      "riskSubtype": "string",
      "riskType": "string",
      "severity": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Available Risks action reference](actions/list-available-risks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upGuard/latest/actions/list-available-risks).

## Send Security Questionnaire To Vendor

Sends a security questionnaire to a vendor in UpGuard.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/send-security-questionnaire-to-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionnaireTypeId": 1,
  "senderEmail": "ava@example.com",
  "dueDate": "string",
  "recipients[]": [
    {}
  ],
  "riskInformationVisibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/send-security-questionnaire-to-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionnaireTypeId": 1,
    "senderEmail": "ava@example.com",
    "dueDate": "string",
    "recipients[]": [{}],
    "riskInformationVisibility": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Send Security Questionnaire To Vendor action reference](actions/send-security-questionnaire-to-vendor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upGuard/latest/actions/send-security-questionnaire-to-vendor).
