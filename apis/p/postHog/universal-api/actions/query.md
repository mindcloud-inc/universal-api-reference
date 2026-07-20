# PostHog: Query

Retrieves query results from a PostHog project.

```
GET https://connect.mindcloud.co/v1/universal/postHog/latest/actions/query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostHog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/query?connectionId=$CONNECTION_ID&projectId=147474" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "147474"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postHog/latest/actions/query?${params}`, {
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
| `query.qry` | string | no |  |
| `query` | object | no |  |
| `query.kind` | string | no | Default: `HogQLQuery`. |
| `async` | string | no |  |
| `projectId` | string | yes | Default: `147474`. |
| `refresh` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_kx": {},
      "$browser": "string",
      "$browser_version": 1,
      "$creator_event_uuid": "string",
      "$current_url": "https://example.com",
      "$device_type": "string",
      "$geoip_accuracy_radius": 1,
      "$geoip_city_confidence": {},
      "$geoip_city_name": "Ava Chen",
      "$geoip_continent_code": "string",
      "$geoip_continent_name": "Ava Chen",
      "$geoip_country_code": "string",
      "$geoip_country_name": "Ava Chen",
      "$geoip_latitude": 1,
      "$geoip_longitude": 1,
      "$geoip_postal_code": "string",
      "$geoip_subdivision_1_code": "string",
      "$geoip_subdivision_1_name": "Ava Chen",
      "$geoip_subdivision_2_code": {},
      "$geoip_subdivision_2_name": {},
      "$geoip_time_zone": "string",
      "$host": "string",
      "$initial__kx": {},
      "$initial_browser": "string",
      "$initial_browser_version": 1,
      "$initial_current_url": "https://example.com",
      "$initial_dclid": {},
      "$initial_device_type": "string",
      "$initial_epik": {},
      "$initial_fbclid": {},
      "$initial_gad_source": {},
      "$initial_gbraid": {},
      "$initial_gclid": {},
      "$initial_gclsrc": {},
      "$initial_geoip_accuracy_radius": 1,
      "$initial_geoip_city_confidence": {},
      "$initial_geoip_city_name": "Ava Chen",
      "$initial_geoip_continent_code": "string",
      "$initial_geoip_continent_name": "Ava Chen",
      "$initial_geoip_country_code": "string",
      "$initial_geoip_country_name": "Ava Chen",
      "$initial_geoip_latitude": 1,
      "$initial_geoip_longitude": 1,
      "$initial_geoip_postal_code": "string",
      "$initial_geoip_subdivision_1_code": "string",
      "$initial_geoip_subdivision_1_name": "Ava Chen",
      "$initial_geoip_subdivision_2_code": {},
      "$initial_geoip_subdivision_2_name": {},
      "$initial_geoip_time_zone": "string",
      "$initial_host": "string",
      "$initial_igshid": {},
      "$initial_irclid": {},
      "$initial_li_fat_id": {},
      "$initial_mc_cid": {},
      "$initial_msclkid": {},
      "$initial_os": "string",
      "$initial_os_version": "string",
      "$initial_pathname": "Ava Chen",
      "$initial_qclid": {},
      "$initial_raw_user_agent": "string",
      "$initial_rdt_cid": {},
      "$initial_referrer": "string",
      "$initial_referring_domain": "string",
      "$initial_sccid": {},
      "$initial_screen_height": 1,
      "$initial_screen_width": 1,
      "$initial_ttclid": {},
      "$initial_twclid": {},
      "$initial_utm_campaign": {},
      "$initial_utm_content": {},
      "$initial_utm_medium": {},
      "$initial_utm_source": {},
      "$initial_utm_term": {},
      "$initial_viewport_height": 1,
      "$initial_viewport_width": 1,
      "$initial_wbraid": {},
      "$os": "string",
      "$os_version": "string",
      "$pathname": "Ava Chen",
      "$raw_user_agent": "string",
      "$referrer": "string",
      "$referring_domain": "string",
      "$screen_height": 1,
      "$screen_width": 1,
      "$viewport_height": 1,
      "$viewport_width": 1,
      "$virt_initial_channel_type": "string",
      "$virt_initial_referring_domain_type": {},
      "companyId": "string",
      "created_at": "string",
      "dclid": {},
      "email": "ava@example.com",
      "epik": {},
      "fbclid": {},
      "gad_source": {},
      "gbraid": {},
      "gclid": {},
      "gclsrc": {},
      "id": "string",
      "igshid": {},
      "irclid": {},
      "is_identified": 1,
      "li_fat_id": {},
      "mc_cid": {},
      "msclkid": {},
      "qclid": {},
      "rdt_cid": {},
      "sccid": {},
      "ttclid": {},
      "twclid": {},
      "username": "Ava Chen",
      "utm_campaign": {},
      "utm_content": {},
      "utm_medium": {},
      "utm_source": {},
      "utm_term": {},
      "wbraid": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_kx` | object |  |
| `$browser` | string |  |
| `$browser_version` | number |  |
| `$creator_event_uuid` | string |  |
| `$current_url` | string |  |
| `$device_type` | string |  |
| `$geoip_accuracy_radius` | number |  |
| `$geoip_city_confidence` | object |  |
| `$geoip_city_name` | string |  |
| `$geoip_continent_code` | string |  |
| `$geoip_continent_name` | string |  |
| `$geoip_country_code` | string |  |
| `$geoip_country_name` | string |  |
| `$geoip_latitude` | number |  |
| `$geoip_longitude` | number |  |
| `$geoip_postal_code` | string |  |
| `$geoip_subdivision_1_code` | string |  |
| `$geoip_subdivision_1_name` | string |  |
| `$geoip_subdivision_2_code` | object |  |
| `$geoip_subdivision_2_name` | object |  |
| `$geoip_time_zone` | string |  |
| `$host` | string |  |
| `$initial__kx` | object |  |
| `$initial_browser` | string |  |
| `$initial_browser_version` | number |  |
| `$initial_current_url` | string |  |
| `$initial_dclid` | object |  |
| `$initial_device_type` | string |  |
| `$initial_epik` | object |  |
| `$initial_fbclid` | object |  |
| `$initial_gad_source` | object |  |
| `$initial_gbraid` | object |  |
| `$initial_gclid` | object |  |
| `$initial_gclsrc` | object |  |
| `$initial_geoip_accuracy_radius` | number |  |
| `$initial_geoip_city_confidence` | object |  |
| `$initial_geoip_city_name` | string |  |
| `$initial_geoip_continent_code` | string |  |
| `$initial_geoip_continent_name` | string |  |
| `$initial_geoip_country_code` | string |  |
| `$initial_geoip_country_name` | string |  |
| `$initial_geoip_latitude` | number |  |
| `$initial_geoip_longitude` | number |  |
| `$initial_geoip_postal_code` | string |  |
| `$initial_geoip_subdivision_1_code` | string |  |
| `$initial_geoip_subdivision_1_name` | string |  |
| `$initial_geoip_subdivision_2_code` | object |  |
| `$initial_geoip_subdivision_2_name` | object |  |
| `$initial_geoip_time_zone` | string |  |
| `$initial_host` | string |  |
| `$initial_igshid` | object |  |
| `$initial_irclid` | object |  |
| `$initial_li_fat_id` | object |  |
| `$initial_mc_cid` | object |  |
| `$initial_msclkid` | object |  |
| `$initial_os` | string |  |
| `$initial_os_version` | string |  |
| `$initial_pathname` | string |  |
| `$initial_qclid` | object |  |
| `$initial_raw_user_agent` | string |  |
| `$initial_rdt_cid` | object |  |
| `$initial_referrer` | string |  |
| `$initial_referring_domain` | string |  |
| `$initial_sccid` | object |  |
| `$initial_screen_height` | number |  |
| `$initial_screen_width` | number |  |
| `$initial_ttclid` | object |  |
| `$initial_twclid` | object |  |
| `$initial_utm_campaign` | object |  |
| `$initial_utm_content` | object |  |
| `$initial_utm_medium` | object |  |
| `$initial_utm_source` | object |  |
| `$initial_utm_term` | object |  |
| `$initial_viewport_height` | number |  |
| `$initial_viewport_width` | number |  |
| `$initial_wbraid` | object |  |
| `$os` | string |  |
| `$os_version` | string |  |
| `$pathname` | string |  |
| `$raw_user_agent` | string |  |
| `$referrer` | string |  |
| `$referring_domain` | string |  |
| `$screen_height` | number |  |
| `$screen_width` | number |  |
| `$viewport_height` | number |  |
| `$viewport_width` | number |  |
| `$virt_initial_channel_type` | string |  |
| `$virt_initial_referring_domain_type` | object |  |
| `companyId` | string |  |
| `created_at` | string |  |
| `dclid` | object |  |
| `email` | string |  |
| `epik` | object |  |
| `fbclid` | object |  |
| `gad_source` | object |  |
| `gbraid` | object |  |
| `gclid` | object |  |
| `gclsrc` | object |  |
| `id` | string |  |
| `igshid` | object |  |
| `irclid` | object |  |
| `is_identified` | number |  |
| `li_fat_id` | object |  |
| `mc_cid` | object |  |
| `msclkid` | object |  |
| `qclid` | object |  |
| `rdt_cid` | object |  |
| `sccid` | object |  |
| `ttclid` | object |  |
| `twclid` | object |  |
| `username` | string |  |
| `utm_campaign` | object |  |
| `utm_content` | object |  |
| `utm_medium` | object |  |
| `utm_source` | object |  |
| `utm_term` | object |  |
| `wbraid` | object |  |

## Native endpoint

Through the native PostHog API, this operation is `POST /projects/:projectId/query/` (base URL `https://us.posthog.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query.md) for the provider-specific parameters and requirements.

