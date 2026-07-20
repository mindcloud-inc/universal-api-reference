# GrowthBook: Get all dashboards for an experiment

Retrieves dashboards for a GrowthBook experiment.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-dashboards-for-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-dashboards-for-experiment?connectionId=$CONNECTION_ID&experimentId=experiment_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "experiment_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-dashboards-for-experiment?${params}`, {
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
| `experimentId` | string | yes | Default: `experiment_1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dashboards": [
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
| `dashboards` | array<object> |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /dashboards/by-experiment/:experimentId` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboards-for-experiment.md) for the provider-specific parameters and requirements.

