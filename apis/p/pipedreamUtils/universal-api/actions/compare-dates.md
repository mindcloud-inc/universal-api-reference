# Pipedream Utils: Formatting - [Date/Time] Compare Dates

Compares two dates and their duration in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/compare-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/compare-dates?connectionId=$CONNECTION_ID&inputDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/compare-dates?${params}`, {
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
| `inputDate` | string | yes | Enter start date string, in the format defined in `Input Format`. If the start date is after the end date, these dates will be swapped and in the output `datesSwapped` will be set to `true`. |
| `endDate` | string | yes | Enter end date string, in the format defined in `Input Format`. Timezone is assumed the same for both dates if not explicitly set. |
| `inputFormat` | string | no | The format of the input date strings. If omitted, the parser will try to infer it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datesSwapped": true,
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datesSwapped` | boolean |  |
| `result` | string |  |

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-dates.md) for the provider-specific parameters and requirements.

