# Castor EDC: List Export Jobs

Retrieves export jobs from Castor EDC by study.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-export-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-export-jobs?connectionId=$CONNECTION_ID&study_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "study_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-export-jobs?${params}`, {
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
| `page` | number | no | The page to retrieve |
| `page_size` | number | no | The size of pages |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "completed_on": {
        "date": "string",
        "timezone": "string",
        "timezone_type": 1
      },
      "created_by": "string",
      "created_on": {
        "date": "string",
        "timezone": "string",
        "timezone_type": 1
      },
      "expires_on": {
        "date": "string",
        "timezone": "string",
        "timezone_type": 1
      },
      "export_name": "Ava Chen",
      "export_type": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string |  |
| `completed_on.date` | string |  |
| `completed_on.timezone` | string |  |
| `completed_on.timezone_type` | number |  |
| `created_by` | string |  |
| `created_on.date` | string |  |
| `created_on.timezone` | string |  |
| `created_on.timezone_type` | number |  |
| `expires_on.date` | string |  |
| `expires_on.timezone` | string |  |
| `expires_on.timezone_type` | number |  |
| `export_name` | string |  |
| `export_type` | string |  |
| `file_name` | string |  |
| `file_size` | number |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/export` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-export-jobs.md) for the provider-specific parameters and requirements.

