# Cerbo: List Encounter Types

Retrieves encounter types from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounter-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounter-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounter-types?${params}`, {
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
| `include_deleted` | boolean | no | When set to any truthy value, includes soft-deleted encounter types in the response. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedby": 1,
      "description": "string",
      "encounter_type": "string",
      "is_face_to_face": true,
      "name": "Ava Chen",
      "place_of_service_code": "string",
      "provider_taxonomy": "string",
      "sort_priority": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedby` | number |  |
| `description` | string |  |
| `encounter_type` | string |  |
| `is_face_to_face` | boolean |  |
| `name` | string |  |
| `place_of_service_code` | string |  |
| `provider_taxonomy` | string |  |
| `sort_priority` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /encounter_types` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-encounter-types.md) for the provider-specific parameters and requirements.

