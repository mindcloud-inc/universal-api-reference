# e-Gov: List Licenses

Retrieves dataset licenses from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-licenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-licenses?${params}`, {
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
      "domain_content": "string",
      "domain_data": "string",
      "domain_software": "string",
      "family": "string",
      "id": "string",
      "is_generic": "string",
      "is_okd_compliant": true,
      "is_osi_compliant": true,
      "maintainer": "string",
      "od_conformance": "string",
      "osd_conformance": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain_content` | string |  |
| `domain_data` | string |  |
| `domain_software` | string |  |
| `family` | string |  |
| `id` | string |  |
| `is_generic` | string |  |
| `is_okd_compliant` | boolean |  |
| `is_osi_compliant` | boolean |  |
| `maintainer` | string |  |
| `od_conformance` | string |  |
| `osd_conformance` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /license_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-licenses.md) for the provider-specific parameters and requirements.

