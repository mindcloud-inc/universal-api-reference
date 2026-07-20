# Less Annoying CRM: List Pipelines



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipelines?${params}`, {
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
| `includeArchivedPipelines` | boolean | no | Whether to include archived pipelines. |
| `includeCustomFields` | boolean | no | Whether to include custom field metadata. |
| `includeHiddenPipelines` | boolean | no | Whether admins should include hidden pipelines. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "image": "string",
      "isHidden": true,
      "name": "Ava Chen",
      "permissions": "string",
      "pipelineId": "string",
      "statuses": [
        {
          "color": "string",
          "isActive": true,
          "name": "Ava Chen",
          "statusId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `dateCreated` | date |  |
| `image` | string |  |
| `isHidden` | boolean |  |
| `name` | string |  |
| `permissions` | string |  |
| `pipelineId` | string |  |
| `statuses[].color` | string |  |
| `statuses[].isActive` | boolean |  |
| `statuses[].name` | string |  |
| `statuses[].statusId` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

