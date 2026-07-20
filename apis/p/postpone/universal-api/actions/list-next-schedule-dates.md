# Postpone: List Next Schedule Dates

Retrieves next scheduled post dates from Postpone.

```
GET https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-next-schedule-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-next-schedule-dates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-next-schedule-dates?${params}`, {
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
| `variables.socialAccountIds[]` | array<string> | no | Optional list of social account IDs to filter schedule dates for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleDate": "2026-05-07T12:00:00.000Z",
      "socialAccountId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scheduleDate` | date |  |
| `socialAccountId` | string |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-next-schedule-dates.md) for the provider-specific parameters and requirements.

