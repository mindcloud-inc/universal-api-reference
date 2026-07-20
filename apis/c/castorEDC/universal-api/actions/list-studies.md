# Castor EDC: List Studies

Retrieves studies the current Castor EDC user can access.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-studies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-studies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-studies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "created_by": "string",
      "created_on": "string",
      "crf_id": "string",
      "domain": "string",
      "encryption": true,
      "expected_centers": 1,
      "gcp_enabled": true,
      "live": true,
      "main_contact": "string",
      "name": "Ava Chen",
      "on_site_epro_mode_enabled": true,
      "premium_support_enabled": true,
      "randomization_enabled": true,
      "slug": "string",
      "study_id": "string",
      "surveys_enabled": true,
      "trial_registry_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string |  |
| `created_by` | string |  |
| `created_on` | string |  |
| `crf_id` | string |  |
| `domain` | string |  |
| `encryption` | boolean |  |
| `expected_centers` | number |  |
| `gcp_enabled` | boolean |  |
| `live` | boolean |  |
| `main_contact` | string |  |
| `name` | string |  |
| `on_site_epro_mode_enabled` | boolean |  |
| `premium_support_enabled` | boolean |  |
| `randomization_enabled` | boolean |  |
| `slug` | string |  |
| `study_id` | string |  |
| `surveys_enabled` | boolean |  |
| `trial_registry_id` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-studies.md) for the provider-specific parameters and requirements.

