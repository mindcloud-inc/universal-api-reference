# Startquestion: Get Respondent Batch

Retrieves a Startquestion respondent batch by ID.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-batch?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-batch?${params}`, {
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
| `batchId` | string | yes | Batch ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "id": "string",
      "patches": [
        "string"
      ],
      "survey_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number | Account ID. |
| `id` | string | Batch ID. |
| `patches` | array<string> | Assigned patch IDs. |
| `survey_id` | number | Survey ID. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /respondents/batch` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-respondent-batch.md) for the provider-specific parameters and requirements.

