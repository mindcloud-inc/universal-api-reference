# Reamaze: Get Tags Report



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-tags-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-tags-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-tags-report?${params}`, {
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
| `startDate` | date | no | The `start_date` value can used to choose the start of the report. |
| `endDate` | date | no | The `end_date` value can used to choose the end of the report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "red": 1,
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `red` | number |  |
| `startDate` | string |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /reports/tags` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tags-report.md) for the provider-specific parameters and requirements.

