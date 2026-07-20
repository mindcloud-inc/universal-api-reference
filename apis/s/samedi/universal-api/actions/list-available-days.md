# Samedi: List Available Days

Retrieves available appointment days from Samedi.

```
GET https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-available-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samedi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-available-days?connectionId=$CONNECTION_ID&eventCategoryId=string&eventTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventCategoryId": "string",
  "eventTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-available-days?${params}`, {
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
| `eventCategoryId` | string | yes | Appointment category ID to search available days for. |
| `eventTypeId` | string | yes | Appointment type ID to search available days for. |
| `date` | date | no | Optional date used to return available days for the date's month. |
| `from` | date | no | Optional start date for availability range. |
| `to` | date | no | Optional end date for availability range. |
| `insuranceId` | string | no | Optional insurance company ID used to filter available days. |
| `bornOn` | date | no | Optional patient birth date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samedi API returns.

## Native endpoint

Through the native Samedi API, this operation is `GET /booking/v3/dates` (base URL `https://patient.samedi.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-days.md) for the provider-specific parameters and requirements.

