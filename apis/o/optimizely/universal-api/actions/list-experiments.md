# Optimizely: List Experiments

Retrieves a list of experiments from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-experiments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-experiments?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-experiments?${params}`, {
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
| `projectId` | string | yes | Filter experiments to one project. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "created": "string",
      "description": "string",
      "featureId": 1,
      "id": 1,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "projectId": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `created` | string |  |
| `description` | string |  |
| `featureId` | number |  |
| `id` | number |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /experiments` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-experiments.md) for the provider-specific parameters and requirements.

