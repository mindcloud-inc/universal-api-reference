# DailyMed: List Application Numbers

Retrieves application numbers from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-application-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-application-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-application-numbers?${params}`, {
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
| `applicationNumber` | string | no | Application number of a drug. |
| `marketingCategoryCode` | string | no | Marketing category code of a drug. |
| `setid` | string | no | Set ID of a label. Default: `4543e156-1deb-666e-e063-6394a90a719c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application_number": "string",
      "marketing_category_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_number` | string | Application number. |
| `marketing_category_code` | string | Marketing category code. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /applicationnumbers.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-application-numbers.md) for the provider-specific parameters and requirements.

