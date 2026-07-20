# Bitly: Get Organization Shorten Counts By Group

Retrieves organization shorten counts by group in Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-shorten-counts-by-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-shorten-counts-by-group?connectionId=$CONNECTION_ID&organizationGuid=string&unit=string&units=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationGuid": "string",
  "unit": "string",
  "units": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-shorten-counts-by-group?${params}`, {
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
| `organizationGuid` | string | yes |  |
| `unit` | string | yes |  |
| `unitReference` | string | no |  |
| `units` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "facet": "string",
      "metrics": [
        {
          "key": "string",
          "value": 1
        }
      ],
      "unit": "string",
      "unitReference": "string",
      "units": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `facet` | string |  |
| `metrics[].key` | string |  |
| `metrics[].value` | number |  |
| `unit` | string |  |
| `unitReference` | string |  |
| `units` | number |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /organizations/:organization_guid/shorten_counts_by_group` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-shorten-counts-by-group.md) for the provider-specific parameters and requirements.

