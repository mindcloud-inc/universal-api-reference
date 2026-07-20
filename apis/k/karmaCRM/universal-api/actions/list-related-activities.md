# Karma CRM: List Related Activities

Retrieves activities related to a contact in Karma CRM.

```
GET https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-related-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-related-activities?connectionId=$CONNECTION_ID&recordId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-related-activities?${params}`, {
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
| `page` | number | no | Page number to retrieve. |
| `perPage` | number | no | Number of activities per page. |
| `recordId` | number | yes | The related record ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Karma CRM API returns.

## Native endpoint

Through the native Karma CRM API, this operation is `GET /api/v3/activities/related.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-related-activities.md) for the provider-specific parameters and requirements.

