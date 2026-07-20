# PlumDocs: Get Workflow Fields

Retrieves workflow field definitions from PlumDocs.

```
GET https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-workflow-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlumDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-workflow-fields?connectionId=$CONNECTION_ID&id=wf_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "wf_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-workflow-fields?${params}`, {
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
| `id` | string | yes | The PlumDocs workflow id. Example: `wf_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
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
| `fields` | array<object> | Workflow placeholder definitions |

## Native endpoint

Through the native PlumDocs API, this operation is `GET /workflows/:id/fields` (base URL `https://plumdocs.com/api/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-fields.md) for the provider-specific parameters and requirements.

