# Veracity Learning: Get Activity Profile Document

Retrieves an activity profile document from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-activity-profile-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-activity-profile-document?connectionId=$CONNECTION_ID&activityId=string&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string",
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-activity-profile-document?${params}`, {
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
| `activityId` | string | yes | Target activity IRI. |
| `profileId` | string | yes | Exact activity profile document identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /activities/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-profile-document.md) for the provider-specific parameters and requirements.

