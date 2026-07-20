# SatisMeter: Get Survey



```
GET https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey?connectionId=$CONNECTION_ID&campaignId=61fce0adea447e24ec27d609&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "61fce0adea447e24ec27d609",
  "projectId": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey?${params}`, {
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
| `campaignId` | string | yes | Survey ID. Example: `61fce0adea447e24ec27d609`. |
| `projectId` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Survey ID. |
| `name` | string | Survey name. |
| `state` | string | Survey state. |
| `type` | string | Survey type. |

## Native endpoint

Through the native SatisMeter API, this operation is `GET /api/v3/projects/:projectId/campaigns/:campaignId` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

