# Alto: Get Lead

Retrieves a lead from Alto by ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-lead?${params}`, {
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
| `leadId` | string | yes | Unique Alto lead identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "enquiryDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "leadSource": "string",
      "leadStatus": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdDate` | date |  |
| `enquiryDate` | date |  |
| `id` | string |  |
| `leadSource` | string |  |
| `leadStatus` | string |  |
| `modifiedDate` | date |  |

## Native endpoint

Through the native Alto API, this operation is `GET /leads/:leadId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

