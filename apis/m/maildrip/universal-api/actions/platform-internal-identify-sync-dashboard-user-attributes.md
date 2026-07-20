# Maildrip: Platform-internal identify — sync dashboard user attributes



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/platform-internal-identify-sync-dashboard-user-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/platform-internal-identify-sync-dashboard-user-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/platform-internal-identify-sync-dashboard-user-attributes', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Accepted for contract parity but ignored — authenticated user's email is used |
| `firstName` | string | no | Contact's first name |
| `lastName` | string | no | Contact's last name |
| `traits` | object | no | Arbitrary key-value attributes. Keys are automatically prefixed with `md_` before storage. Keys must be alphanumeric with underscores/hyphens. Values must be primitives: string, number, or boolean. Maximum 10 traits per call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/platform/identify` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/platform-internal-identify-sync-dashboard-user-attributes.md) for the provider-specific parameters and requirements.

