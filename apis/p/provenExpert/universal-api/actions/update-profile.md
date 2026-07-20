# ProvenExpert: Update Profile

Updates your profile in ProvenExpert.

```
PUT https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile', {
  method: 'PUT',
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
| `data.public` | number | no | Whether the profile should be public after the update. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "contact": {
        "country": "string",
        "email": "ava@example.com"
      },
      "created": 1,
      "customerId": 1,
      "email": "ava@example.com",
      "expirePlan": "string",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "plan": "string",
      "profileUrl": "https://example.com",
      "public": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company or profile display name. |
| `contact.country` | string | Contact country code. |
| `contact.email` | string | Contact email address. |
| `created` | number | Unix timestamp for when the profile was created. |
| `customerId` | number | ProvenExpert customer identifier. |
| `email` | string | Primary profile email address. |
| `expirePlan` | string | Plan that applies after expiry. |
| `expiryDate` | date | Date when the current plan expires. |
| `plan` | string | Current ProvenExpert plan name. |
| `profileUrl` | string | Public ProvenExpert profile URL. |
| `public` | number | Profile visibility flag from the API response. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /profile/update` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-profile.md) for the provider-specific parameters and requirements.

