# Omniconvert Explore: Get Experiment

Retrieves an experiment from Omniconvert Explore.

```
GET https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omniconvert Explore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-experiment?connectionId=$CONNECTION_ID&experimentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/get-experiment?${params}`, {
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
| `experimentId` | number | yes | Identifier of the experiment taken from the experiments list. |
| `filter` | string | no | Experiment detail filter carrier documented by Omniconvert (interval-start, interval-end). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omniconvert Explore API returns.

## Native endpoint

Through the native Omniconvert Explore API, this operation is `GET /experiments/:experimentId` (base URL `https://api.omniconvert.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment.md) for the provider-specific parameters and requirements.

