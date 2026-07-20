# SigningHub: Get Package Timeline

Retrieves package timeline details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-timeline?connectionId=$CONNECTION_ID&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-package-timeline?${params}`, {
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
| `packageId` | number | yes | Package ID of the document package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "package_name": "Ava Chen",
      "process_status": "string",
      "processed_on": "2026-05-07T12:00:00.000Z",
      "shared_on": "2026-05-07T12:00:00.000Z",
      "time_taken": {},
      "timeline_details": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `package_name` | string |  |
| `process_status` | string |  |
| `processed_on` | date |  |
| `shared_on` | date |  |
| `time_taken` | object |  |
| `timeline_details` | array<object> |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/workflow/timeline` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-timeline.md) for the provider-specific parameters and requirements.

