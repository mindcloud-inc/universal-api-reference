# Atlar: Get facility activity

Retrieves a facility activity from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility-activity?connectionId=$CONNECTION_ID&id=string&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility-activity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string<string> | yes |  |
| `activityId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "created": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "facilityId": "string",
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
      "version": 1
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
| `facilityId` | string |  |
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

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2beta/facilities/{id}/activities/{activityId}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facility-activity.md) for the provider-specific parameters and requirements.

