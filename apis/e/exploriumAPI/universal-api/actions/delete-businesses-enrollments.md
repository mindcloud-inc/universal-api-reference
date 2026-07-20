# Explorium: Delete Businesses Enrollments

Deletes business event enrollments from Explorium API.

```
DELETE https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/delete-businesses-enrollments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/delete-businesses-enrollments?connectionId=$CONNECTION_ID&business_ids%5B%5D=string&enrollment_key=string&event_types%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_ids[]": "string",
  "enrollment_key": "string",
  "event_types[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/delete-businesses-enrollments?${params}`, {
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
| `business_ids[]` | array<string> | yes | The Explorium business identifiers to enroll. |
| `enrollment_key` | string | yes | The client-defined enrollment key. |
| `event_types[]` | array<string> | yes | The business event types to enroll for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Explorium response metadata. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/businesses/events/enrollments` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-businesses-enrollments.md) for the provider-specific parameters and requirements.

