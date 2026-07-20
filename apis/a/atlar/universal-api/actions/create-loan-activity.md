# Atlar: Create loan activity

Creates a loan activity in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loanId": "string",
  "type": "string",
  "amount": {},
  "localDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loanId": "string",
    "type": "string",
    "amount": {},
    "localDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loanId` | string<string> | yes |  |
| `type` | string<string> | yes |  |
| `amount` | object<string> | yes |  |
| `localDate` | date<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "created": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "id": "string",
      "loanId": "string",
      "localDate": "2026-05-07T12:00:00.000Z",
      "organizationId": "string",
      "origin": {},
      "periodEnd": "2026-05-07T12:00:00.000Z",
      "periodStart": "2026-05-07T12:00:00.000Z",
      "rate": "string",
      "reference": "string",
      "settlements": [
        {}
      ],
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "weightedRate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `created` | date |  |
| `etag` | string |  |
| `id` | string |  |
| `loanId` | string |  |
| `localDate` | date |  |
| `organizationId` | string |  |
| `origin` | object |  |
| `periodEnd` | date |  |
| `periodStart` | date |  |
| `rate` | string |  |
| `reference` | string |  |
| `settlements` | array<object> |  |
| `timestamp` | date |  |
| `type` | string |  |
| `updated` | date |  |
| `version` | number |  |
| `weightedRate` | string |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /financial-data/v2beta/loans/{loanId}/activities` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-loan-activity.md) for the provider-specific parameters and requirements.

