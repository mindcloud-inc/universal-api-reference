# Zeplin: List Organization Workflow Statuses

Retrieves a list of organization workflow statuses from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-workflow-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-workflow-statuses?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-workflow-statuses?${params}`, {
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
| `organizationId` | string | yes | Organization id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {},
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /organizations/{organization_id}/workflow_statuses` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-workflow-statuses.md) for the provider-specific parameters and requirements.

