# Veracity Learning: List Activity Profile IDs

Lists activity profile IDs from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-activity-profile-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-activity-profile-ids?connectionId=$CONNECTION_ID&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-activity-profile-ids?${params}`, {
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
| `since` | date | no | Return activity profile IDs updated after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "profileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `profileId` | string | Activity profile document identifier available for the requested activity. |

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /activities/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity-profile-ids.md) for the provider-specific parameters and requirements.

