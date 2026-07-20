# Postmark: Create Domain

Creates a domain in Postmark.

```
POST https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-domain', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "DKIMPendingHost": "string",
      "DKIMVerified": true,
      "ID": 1,
      "Name": "Ava Chen",
      "ReturnPathDomain": "string",
      "ReturnPathDomainVerified": true,
      "SPFHost": "string",
      "SPFVerified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DKIMPendingHost` | string |  |
| `DKIMVerified` | boolean |  |
| `ID` | number |  |
| `Name` | string |  |
| `ReturnPathDomain` | string |  |
| `ReturnPathDomainVerified` | boolean |  |
| `SPFHost` | string |  |
| `SPFVerified` | boolean |  |

## Native endpoint

Through the native Postmark API, this operation is `POST /domains` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

