# Content Snare: Submit All Page Fields For Review

Submits all page fields for review in Content Snare.

```
PUT https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/submit-all-page-fields-for-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/submit-all-page-fields-for-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/submit-all-page-fields-for-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Page ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Content Snare API returns.

## Native endpoint

Through the native Content Snare API, this operation is `PUT /partner_api/v1/pages/{id}/submit_all_fields` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-all-page-fields-for-review.md) for the provider-specific parameters and requirements.

