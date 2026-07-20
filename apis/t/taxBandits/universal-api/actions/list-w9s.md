# TaxBandits: List W-9s

Retrieves W-9 records from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-w9s
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-w9s?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-w9s?${params}`, {
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
| `businessId` | string | no | Business identifier. |
| `page` | string | no | Page number. |
| `pageSize` | string | no | Records per page. |
| `tin` | string | no | Business EIN or SSN. |
| `w9Status` | string | no | Filter by W-9 status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        {}
      ],
      "FormW9Records": [
        {}
      ],
      "Page": 1,
      "PageSize": 1,
      "TotalPages": 1,
      "TotalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `FormW9Records` | array<object> |  |
| `Page` | number |  |
| `PageSize` | number |  |
| `TotalPages` | number |  |
| `TotalRecords` | number |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET FormW9/List` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-w9s.md) for the provider-specific parameters and requirements.

