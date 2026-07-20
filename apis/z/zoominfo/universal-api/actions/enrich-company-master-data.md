# Zoominfo: Enrich Company Master Data

Enriches company master data with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company-master-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company-master-data?connectionId=$CONNECTION_ID&matchCompanyInput%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matchCompanyInput[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-company-master-data?${params}`, {
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
| `matchCompanyInput[]` | array<object> | yes | Array of company master match objects using documented fields such as zi_c_url, zi_c_name, phone, address, email, or zi_c_company_id. |
| `outputFields[]` | array<string> | no | Array of response field names to return. Accepts multiple values as an array. Default: `["zi_c_name","zi_c_url","zi_c_location_id"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "zi_c_city": "string",
      "zi_c_country": "string",
      "zi_c_is_hq": "string",
      "zi_c_legal_entity_type": "string",
      "zi_c_location_id": 1,
      "zi_c_name": "Ava Chen",
      "zi_c_name_display": "Ava Chen",
      "zi_c_state": "string",
      "zi_c_street": "string",
      "zi_c_tier_grade": "string",
      "zi_c_url": "https://example.com",
      "zi_c_zip": "string",
      "zi_es_ecid": 1,
      "zi_es_location_id": "string",
      "zi_match_reason": {
        "zi_match_reason_building_name": "Ava Chen",
        "zi_match_reason_building_number": "string",
        "zi_match_reason_business_type": "string",
        "zi_match_reason_city": "string",
        "zi_match_reason_company_phone": "string",
        "zi_match_reason_country": "string",
        "zi_match_reason_directional": "string",
        "zi_match_reason_name": "Ava Chen",
        "zi_match_reason_road_name": "Ava Chen",
        "zi_match_reason_road_type": "string",
        "zi_match_reason_state": "string",
        "zi_match_reason_unit": "string",
        "zi_match_reason_website": "string",
        "zi_match_reason_zip": "string",
        "zi_match_score": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `zi_c_city` | string |  |
| `zi_c_country` | string |  |
| `zi_c_is_hq` | string |  |
| `zi_c_legal_entity_type` | string |  |
| `zi_c_location_id` | number |  |
| `zi_c_name` | string |  |
| `zi_c_name_display` | string |  |
| `zi_c_state` | string |  |
| `zi_c_street` | string |  |
| `zi_c_tier_grade` | string |  |
| `zi_c_url` | string |  |
| `zi_c_zip` | string |  |
| `zi_es_ecid` | number |  |
| `zi_es_location_id` | string |  |
| `zi_match_reason.zi_match_reason_building_name` | string |  |
| `zi_match_reason.zi_match_reason_building_number` | string |  |
| `zi_match_reason.zi_match_reason_business_type` | string |  |
| `zi_match_reason.zi_match_reason_city` | string |  |
| `zi_match_reason.zi_match_reason_company_phone` | string |  |
| `zi_match_reason.zi_match_reason_country` | string |  |
| `zi_match_reason.zi_match_reason_directional` | string |  |
| `zi_match_reason.zi_match_reason_name` | string |  |
| `zi_match_reason.zi_match_reason_road_name` | string |  |
| `zi_match_reason.zi_match_reason_road_type` | string |  |
| `zi_match_reason.zi_match_reason_state` | string |  |
| `zi_match_reason.zi_match_reason_unit` | string |  |
| `zi_match_reason.zi_match_reason_website` | string |  |
| `zi_match_reason.zi_match_reason_zip` | string |  |
| `zi_match_reason.zi_match_score` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/company-master` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company-master-data.md) for the provider-specific parameters and requirements.

