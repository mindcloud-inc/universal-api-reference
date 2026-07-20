# Optimizely: Get Experiment

Retrieves experiment details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment?connectionId=$CONNECTION_ID&experimentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment?${params}`, {
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
| `experimentId` | string | yes | The experiment id. Default: `1`. |

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

Through the native Optimizely API, this operation is `GET /experiments/{experimentId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment.md) for the provider-specific parameters and requirements.

