# VisionFly: Get Usage Statistics

Retrieves usage statistics from VisionFly.

```
GET https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-usage-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-usage-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-usage-statistics?${params}`, {
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
      "bandwidth": {},
      "history": [
        {}
      ],
      "overage": {},
      "plan": "string",
      "projects": {},
      "storage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bandwidth` | object | Bandwidth usage details. |
| `history` | array<object> | Historical monthly usage. |
| `overage` | object | Overage and cost details. |
| `plan` | string | Current VisionFly plan. |
| `projects` | object | Project usage details. |
| `storage` | object | Storage usage details. |

## Native endpoint

Through the native VisionFly API, this operation is `GET /cdn/usage` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-statistics.md) for the provider-specific parameters and requirements.

