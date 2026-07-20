# Samedi: List Appointment Categories

Retrieves appointment categories from Samedi.

```
GET https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-appointment-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samedi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-appointment-categories?connectionId=$CONNECTION_ID&practiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "practiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-appointment-categories?${params}`, {
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
| `practiceId` | string | yes | Institution/practice ID to list appointment categories for. |
| `insuranceId` | string | no | Optional insurance company ID used to filter appointment categories. |
| `bornOn` | date | no | Optional patient birth date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samedi API returns.

## Native endpoint

Through the native Samedi API, this operation is `GET /booking/v3/event_categories` (base URL `https://patient.samedi.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointment-categories.md) for the provider-specific parameters and requirements.

