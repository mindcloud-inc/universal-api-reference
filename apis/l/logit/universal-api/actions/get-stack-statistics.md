# Logit: Get Stack Statistics

Retrieves stack statistics from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-statistics?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-statistics?${params}`, {
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
| `stackId` | string | yes | The ID of a Logit stack. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "planVolume": 1,
      "planVolumeDisplay": "string",
      "stackType": "string",
      "totalSent": 1,
      "volumeSent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `planVolume` | number |  |
| `planVolumeDisplay` | string |  |
| `stackType` | string |  |
| `totalSent` | number |  |
| `volumeSent` | number |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/statistics` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-statistics.md) for the provider-specific parameters and requirements.

