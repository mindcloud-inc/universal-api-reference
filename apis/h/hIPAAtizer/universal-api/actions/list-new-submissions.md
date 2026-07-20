# HIPAAtizer: List New Submissions

Retrieves new submissions from HIPAAtizer by workflow or location.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-new-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-new-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-new-submissions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.locationIds` | list<string> | no | Optional location UUID filters. |
| `request.workflowIds` | list<string> | no | Optional workflow UUID filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "id": "string",
        "locationId": "string",
        "workflowId": "string"
      },
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.id` | string |  |
| `data.locationId` | string |  |
| `data.workflowId` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `POST /api/v1/api_key/submissions/unconfirmed_list` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-submissions.md) for the provider-specific parameters and requirements.

