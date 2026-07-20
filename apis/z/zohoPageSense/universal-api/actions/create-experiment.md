# Zoho PageSense: Create Experiment

Creates an experiment in Zoho PageSense.

```
POST https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "experiment.displayName": "Ava Chen",
  "experiment.experimentUrl": "https://example.com",
  "experiment.experimentType": 1,
  "experiment.projectLinkname": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-experiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "experiment.displayName": "Ava Chen",
    "experiment.experimentUrl": "https://example.com",
    "experiment.experimentType": 1,
    "experiment.projectLinkname": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `experiment.displayName` | string | yes | Human-readable experiment name. |
| `experiment.experimentUrl` | string | yes | URL included in the experiment configuration. |
| `experiment.experimentType` | number | yes | Experiment type code from Zoho PageSense. |
| `experiment.projectLinkname` | string | yes | Project linkname for the experiment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "experiments": [
        {
          "displayName": "Ava Chen",
          "experimentId": "string",
          "experimentKey": "string",
          "linkname": "https://example.com",
          "projectLinkname": "https://example.com",
          "success": true
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `experiments[].displayName` | string |  |
| `experiments[].experimentId` | string |  |
| `experiments[].experimentKey` | string |  |
| `experiments[].linkname` | string |  |
| `experiments[].projectLinkname` | string |  |
| `experiments[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `POST /portal/:portalName/experiments` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-experiment.md) for the provider-specific parameters and requirements.

