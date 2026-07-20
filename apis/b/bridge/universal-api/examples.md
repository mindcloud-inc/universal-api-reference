# Bridge Universal API Examples

These examples use the MindCloud API key and Bridge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Providers

Retrieves supported providers from Bridge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-providers?${params}`, {
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

See the full [List Providers action reference](actions/list-providers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bridge/latest/actions/list-providers).

## Collect User Consent for Guidance Services

Collects user consent for guidance services in Bridge.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/collect-user-consent-for-guidance-services" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userUuid": "string",
  "companyIdentificationNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/collect-user-consent-for-guidance-services', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userUuid": "string",
    "companyIdentificationNumber": "string"
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

See the full [Collect User Consent for Guidance Services action reference](actions/collect-user-consent-for-guidance-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bridge/latest/actions/collect-user-consent-for-guidance-services).
