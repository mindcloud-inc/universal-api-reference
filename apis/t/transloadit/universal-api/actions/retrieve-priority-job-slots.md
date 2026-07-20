# Transloadit: Retrieve currently used priority job slots

Retrieves currently used priority job slots from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-priority-job-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-priority-job-slots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-priority-job-slots?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "ok": "string",
      "priority_job_slots": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for queue slot retrieval. |
| `priority_job_slots` | object | Object describing current priority slot usage. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /queues/job_slots` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-priority-job-slots.md) for the provider-specific parameters and requirements.

