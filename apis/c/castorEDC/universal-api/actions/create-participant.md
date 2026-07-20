# Castor EDC: Create Participant

Creates a participant in Castor EDC.

```
POST https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "study_id": "string",
  "site_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-participant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "study_id": "string",
    "site_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ccr_patient_id` | string | no | Optional clinical identifier |
| `participant_id` | string | no | Participant identifier when the study allows free-text IDs |
| `study_id` | string | yes | The ID of the study for which this call should be made |
| `site_id` | string | yes | Site UUID for the participant |
| `email_address` | string | no | Optional participant email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {
        "site": {
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
      "mobile_my_details_enabled": true,
      "mobile_ui_version": "string",
      "participant_id": "string",
      "progress": 1,
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
| `_embedded.site._links.self.href` | string |  |
| `_embedded.site.abbreviation` | string |  |
| `_embedded.site.country_id` | number |  |
| `_embedded.site.date_display_format` | string |  |
| `_embedded.site.date_format` | string |  |
| `_embedded.site.deleted` | boolean |  |
| `_embedded.site.id` | string |  |
| `_embedded.site.name` | string |  |
| `_embedded.site.order` | number |  |
| `_embedded.site.site_id` | string |  |
| `_links.self.href` | string |  |
| `archived` | boolean |  |
| `ccr_patient_id` | string |  |
| `created_by` | string |  |
| `created_on.date` | string |  |
| `created_on.timezone` | string |  |
| `created_on.timezone_type` | number |  |
| `id` | string |  |
| `locked` | boolean |  |
| `mobile_my_details_enabled` | boolean |  |
| `mobile_ui_version` | string |  |
| `participant_id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `updated_by` | string |  |
| `updated_on.date` | string |  |
| `updated_on.timezone` | string |  |
| `updated_on.timezone_type` | number |  |

## Native endpoint

Through the native Castor EDC API, this operation is `POST /study/:study_id/participant` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-participant.md) for the provider-specific parameters and requirements.

