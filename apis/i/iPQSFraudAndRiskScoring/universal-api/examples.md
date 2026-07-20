# IPQS Fraud and Risk Scoring Universal API Examples

These examples use the MindCloud API key and IPQS Fraud and Risk Scoring connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries

Retrieves country codes and names from IPQS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-countries?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPQSFraudAndRiskScoring/latest/actions/list-countries).

## Create Allowlist Entry

Creates a new allowlist entry in IPQS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/create-allowlist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "1.1.1.1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/create-allowlist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "1.1.1.1"
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

See the full [Create Allowlist Entry action reference](actions/create-allowlist-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPQSFraudAndRiskScoring/latest/actions/create-allowlist-entry).
