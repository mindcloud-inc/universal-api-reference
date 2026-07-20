# Environmental Protection Agency: List Fields By Service

Retrieves field definitions for a selected EPA AQS service.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-fields-by-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-fields-by-service?connectionId=$CONNECTION_ID&service=sampleData" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service": "sampleData"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-fields-by-service?${params}`, {
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
| `service` | string | yes | EPA AQS service name to return field definitions for, such as sampleData or list. Example: `sampleData`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_description": "string",
      "field_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_description` | string | EPA field definition. |
| `field_name` | string | Response field name. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /metaData/fieldsByService` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields-by-service.md) for the provider-specific parameters and requirements.

