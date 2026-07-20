# Vouchsafe: Perform Smart Lookup

Runs smart lookup checks in Vouchsafe.

```
POST https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-smart-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-smart-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "checks[]": "AML"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-smart-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "checks[]": "AML"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Given name(s). |
| `lastName` | string | yes | Family name. |
| `checks[]` | array<string> | yes | The background checks to run. One of: `AML`, `CreditBureau`, `OnlineFootprint`. |
| `firstLineOfAddress` | string | no | Required when checks includes Credit Bureau. |
| `postcode` | string | no | Required when checks includes Credit Bureau. |
| `email` | string | no | Either email or phone is required when checks includes Online Footprint. |
| `phone` | string | no | Either email or phone is required when checks includes Online Footprint. |
| `dateOfBirth` | string | no | Required when checks includes Credit Bureau or AML. |
| `thresholds` | object | no | Optional custom thresholds for AML and Online Footprint checks. |
| `thresholds.aml` | number | no | Minimum score required to pass AML check (0-100). |
| `thresholds.onlineFootprint` | number | no | Minimum score required to pass Online Footprint check (0-100). |
| `alertsEnabled` | boolean | no | When true, enables ongoing AML monitoring for this lookup. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `POST /smart-lookups` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-smart-lookup.md) for the provider-specific parameters and requirements.

