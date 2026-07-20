# Leadboxer: Update Form Tracking

Updates form tracking settings for a dataset in Leadboxer.

```
PUT https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-form-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-form-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formTracking": true,
  "allowIpMasking": true,
  "formInputAttribute": "string",
  "datasetId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-form-tracking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formTracking": true,
    "allowIpMasking": true,
    "formInputAttribute": "string",
    "datasetId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formTracking` | boolean | yes | Whether form tracking is enabled. |
| `allowIpMasking` | boolean | yes | Whether IP masking is allowed. |
| `formInputAttribute` | string | yes | The form input attribute to track. |
| `datasetId` | string | yes | The dataset ID. |
| `email` | string | yes | The user email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `PUT /v1/datasets/{{datasetId}}/form-tracking` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-tracking.md) for the provider-specific parameters and requirements.

