# GrowthBook: Get a list of experiments with names and ids

Retrieves experiment names and IDs from GrowthBook.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-names?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-experiment-names?${params}`, {
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
| `projectId` | string | no | Filter by project id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "experiments": [
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
| `experiments` | array<object> |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /experiment-names` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-names.md) for the provider-specific parameters and requirements.

