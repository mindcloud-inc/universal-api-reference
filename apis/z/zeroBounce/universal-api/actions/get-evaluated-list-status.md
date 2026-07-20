# ZeroBounce: Get Evaluated List Status

Retrieves a list evaluation status from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-evaluated-list-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-evaluated-list-status?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-evaluated-list-status?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abuse": true,
      "activityDataPercentage": 1,
      "catchAllPercentage": 1,
      "doNotMail": true,
      "errorMessage": "string",
      "fileId": "string",
      "invalidPercentage": 1,
      "progress": 1,
      "spamTrap": true,
      "status": "string",
      "totalRiskyPercentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abuse` | boolean | Whether the list is flagged for abuse risk. |
| `activityDataPercentage` | number | Percentage of emails with activity data. |
| `catchAllPercentage` | number | Percentage of catch-all emails in the evaluated list. |
| `doNotMail` | boolean | Whether the list is flagged as do-not-mail. |
| `errorMessage` | string | Provider error message when evaluation fails. |
| `fileId` | string | ZeroBounce file identifier. |
| `invalidPercentage` | number | Percentage of invalid emails in the evaluated list. |
| `progress` | number | Completion progress percentage. |
| `spamTrap` | boolean | Whether the list is flagged for spam traps. |
| `status` | string | Evaluation job status. |
| `totalRiskyPercentage` | number | Total risky email percentage reported by ZeroBounce. |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET https://bulkapi.zerobounce.net/v2/listevaluator/:file_id/` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evaluated-list-status.md) for the provider-specific parameters and requirements.

