# Castor EDC: List Records

Retrieves study records from Castor EDC.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-records?connectionId=$CONNECTION_ID&study_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "study_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-records?${params}`, {
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
| `institute` | string | no | Institute UUID to filter on |
| `study_id` | string | yes | The ID of the study for which this call should be made |
| `page` | number | no | The page to retrieve |
| `archived` | number | no | Filter archived records using 0 or 1 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {
        "institute": {
          "_links": {
            "self": {
              "href": "https://example.com"
            }
          },
          "abbreviation": "string",
          "country_id": 1,
          "date_display_format": "string",
          "date_format": "string",
          "deleted": true,
          "id": "string",
          "name": "Ava Chen",
          "order": 1,
          "site_id": "string"
        }
      },
      "_links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "archived": true,
      "ccr_patient_id": "string",
      "created_by": "string",
      "created_on": {
        "date": "string",
        "timezone": "string",
        "timezone_type": 1
      },
      "id": "string",
      "locked": true,
      "mobile_ui_version": "string",
      "progress": 1,
      "record_id": "string",
      "status": "string",
      "updated_by": "string",
      "updated_on": {
        "date": "string",
        "timezone": "string",
        "timezone_type": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded.institute._links.self.href` | string |  |
| `_embedded.institute.abbreviation` | string |  |
| `_embedded.institute.country_id` | number |  |
| `_embedded.institute.date_display_format` | string |  |
| `_embedded.institute.date_format` | string |  |
| `_embedded.institute.deleted` | boolean |  |
| `_embedded.institute.id` | string |  |
| `_embedded.institute.name` | string |  |
| `_embedded.institute.order` | number |  |
| `_embedded.institute.site_id` | string |  |
| `_links.self.href` | string |  |
| `archived` | boolean |  |
| `ccr_patient_id` | string |  |
| `created_by` | string |  |
| `created_on.date` | string |  |
| `created_on.timezone` | string |  |
| `created_on.timezone_type` | number |  |
| `id` | string |  |
| `locked` | boolean |  |
| `mobile_ui_version` | string |  |
| `progress` | number |  |
| `record_id` | string |  |
| `status` | string |  |
| `updated_by` | string |  |
| `updated_on.date` | string |  |
| `updated_on.timezone` | string |  |
| `updated_on.timezone_type` | number |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/record` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

