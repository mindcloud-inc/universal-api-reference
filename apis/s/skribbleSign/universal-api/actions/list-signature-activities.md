# Skribble Sign: List Signature Activities

Retrieves signature activities from Skribble Sign.

```
GET https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/list-signature-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/list-signature-activities?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/list-signature-activities?${params}`, {
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
| `startDate` | string | yes | Start of the activity date range in yyyy-MM-dd format. |
| `endDate` | string | yes | End of the activity date range in yyyy-MM-dd format. |
| `page` | number | no | Page number starting at 1. |
| `size` | number | no | Number of activities to return per page. |
| `sort` | string | no | Sort order, such as asc or desc. |

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
| `activities` | array<object> | Signature activity records. |
| `current_page` | number | Current page. |
| `size` | number | Page size. |
| `total_items` | number | Total activity items. |
| `total_pages` | number | Total pages. |

## Native endpoint

Through the native Skribble Sign API, this operation is `GET /v2/activities/signatures` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-activities.md) for the provider-specific parameters and requirements.

