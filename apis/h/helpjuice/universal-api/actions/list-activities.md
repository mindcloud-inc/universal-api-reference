# Helpjuice: List Activities

Retrieves activities from Helpjuice.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-activities?${params}`, {
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
| `actionType` | string | no | Filter activities by the action performed, such as create or update. |
| `chronologically` | boolean | no | Return activities ordered from oldest to newest. |
| `olderThan` | number | no | Filter activities that happened before the specified activity id. |
| `ownerId` | number | no | Filter activities by the user who performed them. |
| `reverseChronologically` | boolean | no | Return activities ordered from newest to oldest. |
| `trackableId` | number | no | Filter activities for a specific Helpjuice item id. |
| `trackableType` | string | no | Filter activities by Helpjuice trackable type such as Question or Category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> | The Helpjuice activities returned by the query. |
| `meta` | object | Pagination metadata for the activities collection. |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /activities` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

