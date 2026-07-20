# Survalyzer: List Bounces



```
GET https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-bounces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-bounces?connectionId=$CONNECTION_ID&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-bounces?${params}`, {
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
| `surveyId` | number | yes | Survey identifier whose bounce list should be returned. |
| `panelId` | number | no | Optional panel identifier to scope bounces. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounces": [
        {}
      ],
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounces` | array<object> |  |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Distribute/v3/ReadBounceList` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bounces.md) for the provider-specific parameters and requirements.

