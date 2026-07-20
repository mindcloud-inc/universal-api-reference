# imgix: Get Report

Retrieves a report from imgix.

```
GET https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-report?connectionId=$CONNECTION_ID&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-report?${params}`, {
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
| `reportId` | string | yes | The imgix report id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "completed": true,
          "files": [
            "string"
          ],
          "periodEnd": 1,
          "periodStart": 1,
          "reportKey": "string",
          "reportType": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.completed` | boolean |  |
| `data.attributes.files[]` | string |  |
| `data.attributes.periodEnd` | number |  |
| `data.attributes.periodStart` | number |  |
| `data.attributes.reportKey` | string |  |
| `data.attributes.reportType` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `GET reports/:reportId` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

