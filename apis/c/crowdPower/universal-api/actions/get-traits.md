# CrowdPower: Get Traits

Retrieves traits from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-traits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-traits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-traits?${params}`, {
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
| `q` | string | no | Search query for traits. |
| `type` | string | no | Trait type selector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "deleted_at": 1,
      "description": "string",
      "editable": true,
      "field": "string",
      "format": "string",
      "id": "string",
      "name": "Ava Chen",
      "sort": 1,
      "type": "string",
      "updated_at": 1,
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `deleted_at` | number |  |
| `description` | string |  |
| `editable` | boolean |  |
| `field` | string |  |
| `format` | string |  |
| `id` | string |  |
| `name` | string |  |
| `sort` | number |  |
| `type` | string |  |
| `updated_at` | number |  |
| `visibility` | object |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET projects/{{credentials.projectId}}/traits` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-traits.md) for the provider-specific parameters and requirements.

