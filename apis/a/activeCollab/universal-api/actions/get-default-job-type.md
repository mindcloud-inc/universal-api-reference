# ActiveCollab: Get Default Job Type

Retrieves the default job type from ActiveCollab.

```
GET https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-default-job-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCollab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-default-job-type?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-default-job-type?${params}`, {
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
      "class": "string",
      "defaultHourlyRate": 1,
      "id": 1,
      "isArchived": true,
      "isDefault": true,
      "isInUse": true,
      "name": "Ava Chen",
      "updatedOn": {},
      "urlPath": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `defaultHourlyRate` | number |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `isDefault` | boolean |  |
| `isInUse` | boolean |  |
| `name` | string |  |
| `updatedOn` | object |  |
| `urlPath` | string |  |

## Native endpoint

Through the native ActiveCollab API, this operation is `GET /job-types/default` (base URL `https://app.activecollab.com/:instanceId/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-job-type.md) for the provider-specific parameters and requirements.

