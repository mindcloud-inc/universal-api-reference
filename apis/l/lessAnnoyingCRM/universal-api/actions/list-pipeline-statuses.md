# Less Annoying CRM: List Pipeline Statuses



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-statuses?${params}`, {
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
| `pipelineId` | string | no | Optional pipeline Id to restrict statuses to one pipeline. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "isActive": true,
      "name": "Ava Chen",
      "pipelineId": "string",
      "statusId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `pipelineId` | string |  |
| `statusId` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-statuses.md) for the provider-specific parameters and requirements.

