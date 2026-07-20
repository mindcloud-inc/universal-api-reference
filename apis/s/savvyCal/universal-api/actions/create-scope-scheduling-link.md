# SavvyCal: Create Scope Scheduling Link



```
POST https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/create-scope-scheduling-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/create-scope-scheduling-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeSlug": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/create-scope-scheduling-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeSlug": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeSlug` | string | yes |  |
| `name` | string | yes |  |
| `description` | string | no |  |
| `privateName` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultDuration": 1,
      "description": "string",
      "durations": [
        1
      ],
      "fields": [
        {
          "id": "string",
          "isRequired": true,
          "label": "string",
          "type": "string"
        }
      ],
      "id": "string",
      "increment": 1,
      "name": "Ava Chen",
      "privateName": "Ava Chen",
      "scope": {
        "id": "string",
        "name": "Ava Chen",
        "slug": "string"
      },
      "slug": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultDuration` | number | Default meeting duration in minutes. |
| `description` | string | Link description. |
| `durations[]` | number | Available meeting durations in minutes. |
| `fields[].id` | string | Custom field identifier. |
| `fields[].isRequired` | boolean | Whether the custom field is required. |
| `fields[].label` | string | Custom field label. |
| `fields[].type` | string | Custom field type. |
| `id` | string | Unique scheduling link identifier. |
| `increment` | number | Scheduling increment in minutes. |
| `name` | string | Public link name. |
| `privateName` | string | Private link name. |
| `scope.id` | string | Associated scope identifier. |
| `scope.name` | string | Associated scope name. |
| `scope.slug` | string | Associated scope slug. |
| `slug` | string | Scheduling link slug. |
| `state` | string | Scheduling link state. |

## Native endpoint

Through the native SavvyCal API, this operation is `POST /v1/scopes/:scope_slug/links` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scope-scheduling-link.md) for the provider-specific parameters and requirements.

