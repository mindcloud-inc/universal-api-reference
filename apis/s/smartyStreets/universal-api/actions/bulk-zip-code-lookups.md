# Smarty-streets: Bulk ZIP Code Lookups

Retrieves ZIP Code lookup details from Smarty-streets in bulk.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/bulk-zip-code-lookups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/bulk-zip-code-lookups?connectionId=$CONNECTION_ID&lookups%5B%5D=%5Bobject%20Object%5D%2C%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookups[]": "[object Object],[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/bulk-zip-code-lookups?${params}`, {
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
| `lookups[]` | array<object> | yes | Array of ZIP Code lookup objects. Default: `[{"zipcode":"90210"},{"city":"North Pole","state":"AK"}]`. Example: `[object Object],[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cityStates": [
        {}
      ],
      "inputIndex": 1,
      "zipcodes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cityStates` | array<object> |  |
| `inputIndex` | number |  |
| `zipcodes` | array<object> |  |

## Native endpoint

Through the native Smarty-streets API, this operation is `POST https://us-zipcode.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-zip-code-lookups.md) for the provider-specific parameters and requirements.

