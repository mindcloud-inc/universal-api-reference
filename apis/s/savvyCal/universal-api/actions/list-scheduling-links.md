# SavvyCal: List Scheduling Links



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-scheduling-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-scheduling-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-scheduling-links?${params}`, {
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
| `state` | string | no |  |

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

Through the native SavvyCal API, this operation is `GET /v1/links` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduling-links.md) for the provider-specific parameters and requirements.

