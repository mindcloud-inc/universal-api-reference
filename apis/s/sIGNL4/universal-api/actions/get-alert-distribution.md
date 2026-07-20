# SIGNL4: Get Alert Distribution

Retrieves alert distribution details from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-distribution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-distribution?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-distribution?${params}`, {
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
| `alertId` | string | yes | Alert you want to get the infos from |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distributionId": "string",
      "distributionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distributionId` | string |  |
| `distributionName` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/alerts/{alertId}/distribution` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-distribution.md) for the provider-specific parameters and requirements.

