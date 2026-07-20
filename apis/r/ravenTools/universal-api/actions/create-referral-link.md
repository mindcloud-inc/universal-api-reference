# Raven Tools: Create Referral Link

Creates a new referral link in Raven Tools.

```
POST https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-referral-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-referral-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array with one referral Raven link record to create."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-referral-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array with one referral Raven link record to create."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link` | string | yes | JSON-encoded string for one referral Raven link record. Default: `[{"domain":"codex-raven-tools-verify-20260408.example","status":"active","link url":"https://mindcloud.co/referral","link text":"Referral Raven Link","link type":"Referral","website url":"https://example.com/referral","website type":"Other"}]`. Example: `JSON array with one referral Raven link record to create.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | Created Raven link id. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-referral-link.md) for the provider-specific parameters and requirements.

