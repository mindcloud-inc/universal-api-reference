# Castor EDC: Export Study Data

Exports study data from Castor EDC as a dataset.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/export-study-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/export-study-data?connectionId=$CONNECTION_ID&study_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "study_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/export-study-data?${params}`, {
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
| `study_id` | string | yes | The ID of the study for which this call should be made |
| `exclude_empty_surveys` | boolean | no | Exclude survey instances without data points |
| `exclude_empty_reports` | boolean | no | Exclude report instances without data points |
| `archived` | boolean | no | Include archived data |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/export/data` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-study-data.md) for the provider-specific parameters and requirements.

