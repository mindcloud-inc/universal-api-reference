# Castor EDC: Get Study Statistics

Retrieves study statistics from Castor EDC by study ID.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-study-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-study-statistics?connectionId=$CONNECTION_ID&study_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "study_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-study-statistics?${params}`, {
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
      "records": {
        "institutes": [
          {
            "institute_id": "string",
            "institute_name": "Ava Chen",
            "record_count": 1
          }
        ],
        "total_count": 1
      },
      "study_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string |  |
| `records.institutes[].institute_id` | string |  |
| `records.institutes[].institute_name` | string |  |
| `records.institutes[].record_count` | number |  |
| `records.total_count` | number |  |
| `study_id` | string |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/statistics` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-study-statistics.md) for the provider-specific parameters and requirements.

