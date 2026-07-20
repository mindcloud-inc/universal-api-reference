# Cerbo: List Extended Patient Details

Retrieves extended patient details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-extended-patient-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-extended-patient-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-extended-patient-details?${params}`, {
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
| `id` | number | no | The ID of the patient. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anonymize` | boolean | no | The return values will strip PHI identifiers from the chart including: names, street-level addresses, telephone numbers (area codes will remain), date-of-birth (year of birth will remain) and some questionnaire answers. Because ever client has different questionnaires, you will want to make sure you further anonymize the results if your questionnaires include requests for identifying information |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:id/extended_details` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extended-patient-details.md) for the provider-specific parameters and requirements.

