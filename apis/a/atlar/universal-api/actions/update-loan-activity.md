# Atlar: Update loan activity

Updates an existing loan activity in Atlar.

```
PUT https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loanId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loanId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loanId` | string<string> | yes |  |
| `id` | string<string> | yes |  |
| `If_Match` | string<string> | no |  |

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

Through the native Atlar API, this operation is `PATCH /financial-data/v2beta/loans/{loanId}/activities/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-loan-activity.md) for the provider-specific parameters and requirements.

