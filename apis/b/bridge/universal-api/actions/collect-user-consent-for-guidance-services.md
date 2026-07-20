# Bridge: Collect User Consent for Guidance Services

Collects user consent for guidance services in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/collect-user-consent-for-guidance-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userUuid` | string | yes | The UUID of the user giving consent |
| `companyIdentificationNumber` | string | yes | The identification number of the company (SIREN, ...) (9 digits) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | no | The ISO 3166-1 alpha-2 country code (2 letters) |
| `contactEmail` | string | no | Optional contact email address |
| `contactPhoneNumber` | string | no | Optional contact phone number |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridge API returns.

## Native endpoint

Through the native Bridge API, this operation is `POST /guidance/consents` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-user-consent-for-guidance-services.md) for the provider-specific parameters and requirements.

