# GrowthBook: Get an experiment snapshot status

Retrieves experiment snapshot status from GrowthBook.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-snapshot?connectionId=$CONNECTION_ID&id=prj_19g6smo332up7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prj_19g6smo332up7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-snapshot?${params}`, {
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
| `id` | string | yes | The id of the requested resource (a snapshot ID, not experiment ID) Default: `prj_19g6smo332up7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "snapshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `snapshot` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /snapshots/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-snapshot.md) for the provider-specific parameters and requirements.

