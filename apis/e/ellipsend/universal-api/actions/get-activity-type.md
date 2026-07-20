# Ellipsend: Get Activity Type

Retrieves an activity type from Ellipsend by ID.

```
GET https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-activity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-activity-type?connectionId=$CONNECTION_ID&activityTypeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityTypeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/get-activity-type?${params}`, {
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
| `activityTypeId` | number | yes | The activity type ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ellipsend API returns.

## Native endpoint

Through the native Ellipsend API, this operation is `GET https://api.ellipsend.com/v1/activity-type/[:activity_type_id]` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-type.md) for the provider-specific parameters and requirements.

