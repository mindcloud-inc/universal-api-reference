# Fidel API: Create MID Request

Creates a MID request in Fidel API.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-mid-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-mid-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string",
  "action": "string",
  "locationId": "string",
  "scheme": "string",
  "origin": "string",
  "visaAcquiringMid": "string",
  "visaBin": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-mid-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string",
    "action": "string",
    "locationId": "string",
    "scheme": "string",
    "origin": "string",
    "visaAcquiringMid": "string",
    "visaBin": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programId` | string | yes |  |
| `action` | string | yes | MID request action. |
| `locationId` | string | yes | The location where the MID should be onboarded. |
| `scheme` | string | yes | Card scheme for the MID request. |
| `origin` | string | yes | Source of the MID. |
| `visaAcquiringMid` | string | yes | Visa acquiring MID for brand-provided or processor-provided Visa onboarding. |
| `visaBin` | string | yes | Visa BIN for Visa onboarding. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "action": "string",
      "brandId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "estimatedCompletionDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "live": true,
      "locationId": "string",
      "origin": "string",
      "programId": "string",
      "scheme": "string",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visaAcquiringMid": "string",
      "visaBin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `action` | string |  |
| `brandId` | string |  |
| `created` | date |  |
| `estimatedCompletionDate` | date |  |
| `id` | string |  |
| `live` | boolean |  |
| `locationId` | string |  |
| `origin` | string |  |
| `programId` | string |  |
| `scheme` | string |  |
| `status` | string |  |
| `updated` | date |  |
| `visaAcquiringMid` | string |  |
| `visaBin` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `POST /programs/:programId/mid-requests` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mid-request.md) for the provider-specific parameters and requirements.

