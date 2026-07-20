# Skribble: List Signature Activities

Retrieves signature activities for a business from Skribble.

```
GET https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-activities?connectionId=$CONNECTION_ID&endDate=2026-05-07T12%3A00%3A00.000Z&startDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-05-07T12:00:00.000Z",
  "startDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-activities?${params}`, {
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
| `endDate` | date | yes | End of the activity date range in yyyy-MM-dd format. |
| `page` | number | no | Page number starting at 1. |
| `size` | number | no | Number of activities to return per page. |
| `sort` | string | no | Sort order, such as asc or desc. |
| `startDate` | date | yes | Start of the activity date range in yyyy-MM-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {}
      ],
      "current_page": 1,
      "size": 1,
      "total_items": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> | Signature activity entries. |
| `current_page` | number | Current page number. |
| `size` | number | Page size returned by Skribble. |
| `total_items` | number | Total signature activities available. |
| `total_pages` | number | Total pages available. |

## Native endpoint

Through the native Skribble API, this operation is `GET /v2/activities/signatures` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-activities.md) for the provider-specific parameters and requirements.

