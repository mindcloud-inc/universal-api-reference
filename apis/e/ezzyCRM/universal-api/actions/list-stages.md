# EzzyCRM: List Stages



```
GET https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EzzyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-stages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "stageCode": "string",
          "stageName": "Ava Chen"
        }
      ],
      "pipelineId": 1,
      "pipeLineName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].stageCode` | string |  |
| `data[].stageName` | string |  |
| `pipelineId` | number |  |
| `pipeLineName` | string |  |

## Native endpoint

Through the native EzzyCRM API, this operation is `GET /api/getallstages` (base URL `https://ezzycrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stages.md) for the provider-specific parameters and requirements.

