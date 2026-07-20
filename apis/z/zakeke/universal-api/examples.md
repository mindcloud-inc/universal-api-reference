# Zakeke Universal API Examples

These examples use the MindCloud API key and Zakeke connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Seller Setup Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status?${params}`, {
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
      "connectedWithEStore": true,
      "firstCustomizableProductCreated": true,
      "freeTrialStarted": true,
      "placeTestOrder": true,
      "requirePaymentInformation": true,
      "signupProcessCompleted": true,
      "trialEnd": "string",
      "trialStart": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Seller Setup Status action reference](actions/retrieve-seller-setup-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zakeke/latest/actions/retrieve-seller-setup-status).

## Duplicate Design



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/duplicate-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "000-RE1olDzbT234viB6D11a10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/duplicate-design', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "000-RE1olDzbT234viB6D11a10"
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

See the full [Duplicate Design action reference](actions/duplicate-design.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zakeke/latest/actions/duplicate-design).
