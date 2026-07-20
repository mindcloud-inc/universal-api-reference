# Zoho Creator: Publish Get Records

Retrieves published records from a Zoho Creator report.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-get-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-get-records?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&privateLink=https%3A%2F%2Fexample.com&reportLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "privateLink": "https://example.com",
  "reportLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-get-records?${params}`, {
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
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `criteria` | string | no | Zoho Creator criteria expression used to filter records. |
| `fieldConfig` | string | no | Response field configuration mode. |
| `fields[]` | array<string> | no | Fields to include in the response. |
| `from` | number | no | Starting record offset. |
| `limit` | number | no | Maximum number of records to return. |
| `maxRecords` | number | no | Upper bound on records returned by the query. |
| `privateLink` | string | yes | Zoho Creator publish API private link token. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `data` | array<object> | Published records returned by the selected report. |
| `data[].id` | string | Identifier of a published record returned by the report. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /publish/:account_owner_name/:app_link_name/report/:report_link_name` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-get-records.md) for the provider-specific parameters and requirements.

